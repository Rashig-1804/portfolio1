---
layout: post
codemirror: true
title: Game Runner Examples
description: Learn game development using the GameEngine framework in a contained educational environment. Build game levels, add characters, and create interactive experiences with live code editing and debugging controls.
permalink: /rpg/game

---

## Basic Game: Desert Adventure

{% capture challenge1 %}
Run the basic desert adventure game. Use WASD or arrow keys to move Chill Guy around the desert. Walk up to R2D2 to trigger a mini-game!
{% endcapture %}

{% capture code1 %}
import GameControl from '/assets/js/adventureGame/GameEngine/GameControl.js';
import GameEnvBackground from '/assets/js/adventureGame/GameEngine/GameEnvBackground.js';

class CustomLevel {
    constructor(gameEnv) {
        const path = gameEnv.path;
        const width = gameEnv.innerWidth;
        const height = gameEnv.innerHeight;
        const bgData = {
            name: 'alien_world',
            src: path + "/images/gamebuilder/alien_planet.jpg",
            pixels: { height: 600, width: 1000 }
        };

        const playerData = {
            id: 'Hero',
            src: path + "/images/gamify/tux.png",
            SCALE_FACTOR: 5,
            STEP_FACTOR: 1000,
            ANIMATION_RATE: 50,
            INIT_POSITION: { x: 100, y: 300 },
            pixels: { height: 256, width: 352 },
            orientation: { rows: 8, columns: 11 },
            down: { row: 0, start: 0, columns: 3 },
            downRight: { row: Math.min(1, 8 - 1), start: 0, columns: 3, rotate: Math.PI/16 },
            downLeft: { row: Math.min(2, 8 - 1), start: 0, columns: 3, rotate: -Math.PI/16 },
            right: { row: Math.min(1, 8 - 1), start: 0, columns: 3 },
            left: { row: Math.min(2, 8 - 1), start: 0, columns: 3 },
            up: { row: Math.min(3, 8 - 1), start: 0, columns: 3 },
            upRight: { row: Math.min(1, 8 - 1), start: 0, columns: 3, rotate: -Math.PI/16 },
            upLeft: { row: Math.min(2, 8 - 1), start: 0, columns: 3, rotate: Math.PI/16 },
            hitbox: { widthPercentage: 0.45, heightPercentage: 0.2 },
            keypress: { up: 87, left: 65, down: 83, right: 68 }
        };


        this.classes = [
                  { class: GameEnvBackground, data: bgData }
        ];
    }
}
export { GameControl };
export const gameLevelClasses = [CustomLevel];
{% endcapture %}

{% include game-runner.html
   runner_id="game1"
   challenge=challenge1
   code=code1
   height="150px"
%}
