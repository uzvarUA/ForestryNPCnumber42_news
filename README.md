# ForestryNPCnumber42_news
### Сценарій
Для себе
1. Треба створити папку `dialogue`
2. У ній створити `назва.json`
```js
{
    "format_version": "1.21",
    "minecraft:npc_dialogue": {
        "scenes": [
            {
                "scene_tag": "open",
                "npc_name": {"rawtext":[{"text":"News"}]},
                "text": {"rawtext":[{"text":"Сьогодні новини"}]},
                "buttons": [
                    {
                        "name": {"rawtext":[{"text":"Розказати новин"}]},
						"commands": ["dialogue open @s @initiator news"]
                    }
                ]
            },
            {
                "scene_tag": "news",
                "npc_name": {"rawtext":[{"text":"News"}]},
                "text": {"rawtext":[{"text":"Сьогодні, у лісництві NPC номер 42 /n глобальне похолодання. /n Будьте  обережні!!!"}]},
                "on_close_commands": []
            }
        ]
    }
}
```
3. Виходиш із папки `dialogue`
4. Створити `manifest.json`
```js
{
	"format_version": 1.21,
	"header": {
		"description": "NPC dialogue",
		"name": "NPC dialogue",
		"uuid": "bedb705a-ec8f-458c-b5b9-d9b4fc5a3713",
		"version": [1, 0, 0]
	},
	"modules": [
		{
			"description": "NPC dialogue",
			"type": "data",
			"uuid": "f84b4dcb-7032-4af6-b870-008f2194f619",
			"version": [1, 0, 0]
		}
	]
}
```
5. Для активації треба написати таку команду: `/dialogue change @e[type=npc] open @s`
