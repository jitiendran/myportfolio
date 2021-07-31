<template>
    <div class="about" id="about">
        <div class="header">
            <h3>About</h3>
            <div class="content">
                I am always energetic and eager to learn new skills and new
                technology
            </div>
            <div class="underline"></div>
            <div class="main-grid">
                <div class="my-details">
                    <div class="details">
                        <h3>Jitiendran KS.</h3>
                        <span
                            >Hello, my name is Jitiendran KS. I am a UI Designer
                            and a
                            <span class="grad-text">Frontend Developer</span>
                        </span>
                        <div class="my-skills">
                            <div
                                class="row"
                                v-for="skill in skills"
                                :key="skill"
                            >
                                <div class="skillname">
                                    <img :src="skill.Name" />
                                </div>
                                <div class="skills">
                                    <div
                                        class="skill"
                                        :style="{
                                            background: skill.Color,
                                            width: calculate(skill.level),
                                        }"
                                    ></div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="img"></div>
                </div>
            </div>
        </div>
        <Education />
    </div>
</template>

<script lang="ts">
import Education from "./Education.vue";
export default {
    components: { Education },
    data() {
        return {
            skills: [
                {
                    Name: require("../../assets/icons/angular.png"),
                    Color: "#DF1C35",
                    level: 0.9,
                },
                {
                    Name: require("../../assets/icons/ts.png"),
                    Color: "#1976D2",
                    level: 0.9,
                },
                {
                    Name: require("../../assets/icons/js.png"),
                    Color: "#FED601",
                    level: 0.85,
                },
                {
                    Name: require("../../assets/icons/sass.png"),
                    Color: "#CA6397",
                    level: 0.9,
                },
                {
                    Name: require("../../assets/icons/css.png"),
                    Color: "#0377BC",
                    level: 0.9,
                },
                {
                    Name: require("../../assets/icons/graphql.png"),
                    Color: "#FF4081",
                    level: 0.8,
                },
                {
                    Name: require("../../assets/icons/c++.png"),
                    Color: "#0086D4",
                    level: 0.65,
                },
                {
                    Name: require("../../assets/icons/java.png"),
                    Color: "rgb(245,71,59)",
                    level: 0.5,
                },
                {
                    Name: require("../../assets/icons/python.png"),
                    Color: "#FEC007",
                    level: 0.6,
                },
                {
                    Name: require("../../assets/icons/mysql.png"),
                    Color: "#168F93",
                    level: 0.6,
                },
                {
                    Name: require("../../assets/icons/mongodb.png"),
                    Color: "#4DAF51",
                    level: 0.75,
                },
                {
                    Name: require("../../assets/icons/c.png"),
                    Color: "#3949AB",
                    level: 0.45,
                },
            ],
        };
    },
    methods: {
        filterSkill(skill: string): string {
            return skill === "Cplusplus" ? "C++" : skill;
        },
        calculate(level: number): string {
            return ((level * 100) / 100) * 100 + "%";
        },
    },
};
</script>

<style lang="scss" scoped>
@import "../../scss/abstract";

.about {
    font-family: $primary_font;
    @include smooth-font;
    padding: 2em;
    .header {
        @include flex(
            $direction: column,
            $align-items: center,
            $justify-content: center,
            $gap: 0
        );
        h3 {
            @include font(
                $font-family: $nav-font,
                $font-size: 4.5em,
                $font-weight: 800
            );
        }
        .content {
            color: $primary_color;
            margin-top: 0.75em;
            font-weight: 600;
            font-size: 1.3em;
        }
        .underline {
            margin-top: 1.5em;
            height: 2.2px;
            width: 13em;
            background: $grey;
        }
        .main-grid {
            width: 100%;
            padding: 1em;
            margin-top: 2.5em;
            .my-details {
                display: grid;
                grid-template-columns: repeat(2, 1fr);
                gap: 1em;
                .details {
                    @include flex(
                        $direction: column,
                        $align-items: none,
                        $justify-content: none,
                        $gap: 0.5em
                    );
                    h3 {
                        font-size: 2.3em;
                        font-family: $primary_font;
                        font-weight: 600;
                    }
                    .grad-text {
                        font-weight: 600;
                        @include gradient-text($background: $primary_gradient);
                    }
                    & > span {
                        font-size: 1.5em;
                        font-weight: 500;
                        color: $accent_color;
                        line-height: 1.3;
                    }
                }
                .my-skills {
                    width: 100%;
                    margin-top: 1em;
                    @include flex(
                        $direction: column,
                        $align-items: center,
                        $justify-content: center,
                        $gap: 0.3em
                    );
                    .row {
                        width: 100%;
                        display: flex;
                        align-items: center;
                        gap: 5.5em;
                        .skillname {
                            img {
                                width: 40px;
                                height: 40px;
                            }
                        }
                        .skills {
                            width: 60%;
                            height: 8px;
                            .skill {
                                width: 100%;
                                height: 100%;
                                border-radius: 1em;
                            }
                        }
                    }
                }
                .img {
                    background: url("../../assets/svgs/skill.png");
                    background-repeat: no-repeat;
                    background-size: contain;
                    background-position: center;
                }
            }
        }
    }
    @media all and (max-width: 769px) {
        padding: 1em;
        width: 113%;
        .header {
            .content {
                text-align: center;
            }
            .main-grid {
                .my-details {
                    display: flex;
                    .img {
                        display: none;
                    }
                }
            }
        }
    }
    @media all and (max-width: 426px) {
        width: 166.5%;
    }
    @media all and (max-width: 376px) {
        width: 179.2%;
    }
    @media all and (max-width: 321px) {
        width: 201.5%;
    }
}
</style>
