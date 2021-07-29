<template>
    <div class="education">
        <h3>Education</h3>
        <Timeline :education="educationList" />
    </div>
</template>

<script lang="ts">
import Timeline from "./Timeline.vue";

export default {
    components: { Timeline },
    data() {
        return {
            educationList: [
                {
                    Year: "2018 - Present",
                    InstituteName: "Madras Institutte Of Technology",
                    Program: "B.E Computer Science",
                },
                {
                    Year: "2017 - 2018",
                    InstituteName:
                        "Prince Matriculation Higher Secondary School",
                    Program: "HSC",
                },
                {
                    Year: "2015 - 2016",
                    InstituteName:
                        "Prince Matriculation Higher Secondary School",
                    Program: "SSLC",
                },
            ],
        };
    },
};
</script>

<style lang="scss" scoped>
@import "../../scss/abstract";
.education {
    h3 {
        @include font(
            $font-family: $nav-font,
            $font-size: 4.5em,
            $font-weight: 800
        );
        text-align: center;
    }
}
</style>
