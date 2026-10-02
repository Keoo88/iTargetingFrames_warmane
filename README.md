<p align="center">
  <img src="https://github.com/user-attachments/assets/cdfc0391-6bb4-45dc-9666-bd31e14bc374" alt="iTargetingFrames" width="260">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/iTargetingFrames-WotLK-ff8800?style=for-the-badge&logo=appveyor">
  <img src="https://img.shields.io/badge/WotLK-3.3.5a-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/status-stable-brightgreen?style=for-the-badge">
</p>

<h1 align="center">iTargetingFrames — WotLK 3.3.5a fork</h1>

<p align="center">
  <b>Nameplate targeting frames for World of Warcraft 3.3.5a (WotLK).</b><br>
  <i>Fork of iTargetingFrames, brought back to the 3.3.5a client.</i>
</p>

<p align="center">
  <a href="#english">English</a> ·
  <a href="#russian">Русский</a>
</p>

---

<a name="english"></a>
## English

<p align="center">
  <a href="#features">Features</a> ·
  <a href="#commands">Commands</a> ·
  <a href="#installation">Installation</a> ·
  <a href="#credits">Credits</a>
</p>

### About

**iTargetingFrames** replaces the default enemy nameplates with your own frames —
one frame per visible unit, showing name, health, cast bar, auras, raid icon and a
set of targeting indicators, all with click bindings on top.

This repository is a **fork for the WoW 3.3.5a (WotLK) client**. The original addon
targeted later expansions; here it is adapted to what the 3.3.5a API actually
provides.

<a name="features"></a>
### Features

#### Frame Layout

<img width="902" height="773" alt="settings" src="https://github.com/user-attachments/assets/726736cf-f6b6-46a0-93bb-c8186f6d8901" />

Position, row count, growth direction, spacing, width and height are all yours.
Cap the number of frames you are willing to draw, or leave it uncapped; optionally
hide friendly units entirely or only in combat.

#### Health and Cast Bars

Health bar with class colours or a plain bar colour, optional health text with a
configurable number of decimals and a `%` sign. The cast bar shows the unit name
and the cast, uses its own colour and a separate colour for casts that cannot be
interrupted, and can be detached from the frame and moved anywhere on screen.

#### Auras

Icons for buffs and debuffs, capped by the *Max auras* setting and filtered by a
blacklist. Duration text and stack count, flashing under a configurable number of
seconds at a configurable speed, and sorting by time or by name in either
direction.

#### Indicators

Every frame can carry indicators for **out of combat**, **current target**,
**focus target**, **interrupt range**, **max range (DPS)** and **max range
(utility)** — the range indicators light up per your current specialization's
spell, so you see at a glance who is still reachable.

#### Threat

Aggro, losing aggro and gaining aggro each get their own indicator, weight and
colour.

#### Custom Conditionals

Write your own indicators as plain Lua functions and drive them with the built-in
conditionals — update, aura, cast, health, target change, focus, threat and show.
A set of templates is included to start from, and each conditional has a name, an
invert flag, a weight, a colour and an enable toggle.

#### Bindings

Bind spells, macros, targets and focuses to mouse buttons and keys right on the
frame — including per-class and per-spec binding sets. A warning banner tells you
when you are in keybinding mode, and a "Click me" label marks the frame that is
waiting for a key.


#### Roles and Priority NPCs

Restrict frames by role (tank / all / dps-healer) so you only see what your job
needs. A priority NPC list accepts an NPC id or name plus a comment, and can
optionally accept additions from your group.

#### Appearance

Global and per-part fonts and textures, status-bar and cast-bar textures, frame
background colour, border colour and border size, frame opacity, name colour and
raid icons. Text flags cover none, outline, thick outline and monochrome.

<a name="commands"></a>
### Commands

| Command | Description |
| --- | --- |
| `/itf` | Open the settings window |
| `/itf reset` | Reset everything to defaults |
| `/itf <anything else>` | Print the command help |

<a name="installation"></a>
### Installation

1. Download the latest release (or clone this repository).
2. Unpack the archive.
3. Move the **iTargetingFrames** folder into:
   ```
   \Interface\AddOns\
   ```
4. Enable the addon on the character select screen and start the game.

The final path has to look like `\Interface\AddOns\iTargetingFrames\iTargetingFrames.toc`.

### Compatibility

- Built and tested on **Warmane** (WoW 3.3.5a, Interface `30300`).
- Developed exclusively for **Warmane**. I take no responsibility for other servers.

<a name="credits"></a>
### Credits

- Original addon: **Ironi** — iTargetingFrames
- Backport to WotLK 3.3.5a: **Cheeta**
- This fork: **Keoo** — [discord.gg/sKpJbUrsvR](https://discord.gg/sKpJbUrsvR)

---

<a name="russian"></a>
## Русский

<p align="center">
  <a href="#возможности">Возможности</a> ·
  <a href="#команды">Команды</a> ·
  <a href="#установка">Установка</a> ·
  <a href="#благодарности">Благодарности</a>
</p>

### Об аддоне

**iTargetingFrames** заменяет стандартные таблички противников своими рамками —
по одной на каждого видимого юнита, с именем, здоровьем, полосой каста, аурами,
рейдовой меткой и набором индикаторов наведения, и с привязками кликов поверх
всего этого.

Этот репозиторий — **форк под клиент WoW 3.3.5a (WotLK)**. Оригинальный аддон
писался под более поздние дополнения; здесь он приведён к тому, что реально умеет
API 3.3.5a.

<a name="возможности"></a>
### Возможности

#### Расположение рамок (Frame Layout)

<img width="902" height="773" alt="settings" src="https://github.com/user-attachments/assets/726736cf-f6b6-46a0-93bb-c8186f6d8901" />

Позиция, число строк, направление роста, отступы, ширина и высота — всё
настраивается. Можно ограничить число одновременно рисуемых рамок или не
ограничивать вовсе; дружественные юниты прячутся совсем либо только в бою.

#### Полосы здоровья и каста (Health and Cast Bars)

Полоса здоровья с цветами классов или сплошным цветом, необязательный текст
здоровья с настраиваемым числом знаков после запятой и знаком `%`. Полоса каста
показывает имя юнита и название каста, имеет свой цвет и отдельный цвет для
кастов, которые нельзя прервать, и может быть откреплена от рамки и перенесена
куда угодно на экране.

#### Ауры (Auras)

Иконки баффов и дебаффов с ограничением по числу и с чёрным списком. Текст
длительности и счётчик стаков, мигание ниже заданного числа секунд с настраиваемой
скоростью, сортировка по времени или по имени в любую сторону.

#### Индикаторы (Indicators)

На каждой рамке могут гореть индикаторы **вне боя**, **текущая цель**, **цель
фокуса**, **дистанция прерывания**, **максимальная дистанция (DPS)** и
**максимальная дистанция (утилити)** — индикаторы дистанции считаются по
заклинанию вашего текущего специализации, так что сразу видно, кто ещё доступен.

#### Угроза (Threat)

Агро, потеря агро и набор агро — у каждого свой индикатор, вес и цвет.

#### Пользовательские условия (Custom Conditionals)

Свои индикаторы пишутся обычными функциями на Lua и привязываются к встроенным
условиям — обновление, аура, каст, здоровье, смена цели, фокус, угроза и
появление. В комплекте есть шаблоны, с которых можно начать; у каждого условия
есть имя, флаг инверсии, вес, цвет и переключатель.

#### Привязки (Bindings)

Заклинания, макросы, цели и фокус вешаются на кнопки мыши и клавиши прямо на
рамке — в том числе отдельными наборами для класса и для специализации. Баннер
предупреждает о режиме назначения клавиш, а надпись «Click me» помечает рамку,
которая ждёт нажатия.


#### Роли и приоритетные NPC (Roles and Priority NPCs)

Рамки фильтруются по роли (танк / все / дд-хил), чтобы на экране было только то,
что нужно вашей задаче. Список приоритетных NPC принимает id или имя плюс
комментарий и по желанию разрешает добавления от группы.

#### Внешний вид (Appearance)

Общие и раздельные шрифты и текстуры, текстуры полос и полосы каста, цвет фона
рамки, цвет и толщина рамки, прозрачность рамки, цвет имени и рейдовые метки.
Оформление текста: без обводки, обводка, толстая обводка и монохром.

<a name="команды"></a>
### Команды (Commands)

| Команда | Описание |
| --- | --- |
| `/itf` | Открыть окно настроек |
| `/itf reset` | Сбросить все настройки к значениям по умолчанию |
| `/itf <что угодно ещё>` | Показать справку по командам |

<a name="установка"></a>
### Установка

1. Скачайте последний релиз (или клонируйте репозиторий).
2. Распакуйте архив.
3. Переместите папку **iTargetingFrames** в:
   ```
   \Interface\AddOns\
   ```
4. Включите аддон на экране выбора персонажа и запустите игру.

Итоговый путь должен выглядеть так: `\Interface\AddOns\iTargetingFrames\iTargetingFrames.toc`.

### Совместимость

- Собрано и протестировано на **Warmane** (WoW 3.3.5a, Interface `30300`).
- Разрабатывалось исключительно для **Warmane**. За работоспособность на других серверах ответственности не несу.

<a name="благодарности"></a>
### Благодарности

- Оригинальный аддон: **Ironi** — iTargetingFrames
- Бэкпорт под WotLK 3.3.5a: **Cheeta**
- Этот форк: **Keoo** — [discord.gg/sKpJbUrsvR](https://discord.gg/sKpJbUrsvR)
