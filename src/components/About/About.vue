<template>
    <div class="about">
        <div class="header">
            <h3>About</h3>
            <div class="content">
                I am always energetic and eager to learn new skills and new
                technology
            </div>
            <div class="underline"></div>
            <div class="main-grid">
                <div class="my-details">
                    <span
                        >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;I
                        am Jitiendran. I am currently pursuing B.E Computer
                        Science in Anna University, MIT Campus, Chennai. I did
                        my HSC(Computer Science Group) in Prince Matriculation
                        Higher Secondary School, Chennai.</span
                    >
                    <span
                        >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Though I studied Computer
                        Science in HSC, I had hard time grasping the concepts in
                        the beginning. But eventually I understood the concepts
                        and web development became my favourite concept.</span
                    >
                    <span
                        >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;On December 2020, I
                        joined Datacenter team of our college department as UI
                        developer. Datacenter team's job is to develop an
                        application where all the staff, students can interact.
                        Datacenter team has three teams UI, Angular and
                        Backend(NodeJs,GraphQL).</span
                    >
                    <span
                        >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;I gradually started
                        studying Angular and made several small projects for
                        grasping. Then i made a larger application for creative
                        and innovative project course in Angular. After learning
                        Angular, I started learning GraphQL and NodeJS , So that
                        I can understand the queries made by Datacenter Backend
                        team and started working in Angular.</span
                    >
                    <span
                        >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Rather than techincall
                        skills, I also have studied keyboard for 5 years and I
                        also have a India record for playing
                        keyboard(blindfolded) for seven hours.
                    </span>
                </div>
                <div class="my-skills">
                    <h3>My Skills</h3>
                    <div class="row" v-for="skill in skills" :key="skill">
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
        </div>
    </div>
</template>

<script lang="ts">
export default {
    data: () => {
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
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            .my-skills {
                width: 100%;
                @include flex(
                    $direction: column,
                    $align-items: center,
                    $justify-content: center,
                    $gap: 0.3em
                );
                h3 {
                    @include font(
                        $font-family: inherit,
                        $font-size: 1.5em,
                        $font-weight: 600
                    );
                    margin-bottom: 1em;
                    text-transform: capitalize;
                    color: #2c3e50;
                }
                .row {
                    width: 100%;
                    display: flex;
                    align-items: center;
                    padding: 0em 3em;
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
            .my-details {
                display: flex;
                flex-direction: column;
                gap: 2em;
                padding: 1em 2em;
                & > span {
                    font-size: 1.25em;
                    font-weight: 600;
                    text-align: justify;
                    color: #2c3e50;
                }
            }
        }
    }
}
</style>
