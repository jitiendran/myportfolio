<template>
    <div class="education">
        <div class="header">
            <h3>Education</h3>
            <div class="underline"></div>
        </div>
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
    .header {
        @include flex(
            $direction: column,
            $align-items: center,
            $justify-content: center,
            $gap: 0.2em
        );
        margin-bottom: 2em;
        h3 {
            @include font(
                $font-family: $nav-font,
                $font-size: 4.5em,
                $font-weight: 800
            );
        }
        .underline {
            height: 2.6px;
            width: 9em;
            background: #ccc;
        }
    }
}
</style>
