>Роботу виконала: **Карпик Яна РПЗ-33**

>Дисципліна: Операційні системи

# ЛАБОРАТОРНА РОБОТА №1

## Тема: 
>Знайомство з робочим середовищем віртуальних машин та особливостями операційної системи Linux

## Мета роботи: 
1. Знайомство з гіпервізорами різного типу, віртуалізацією при роботі з операційними системами.
2. Знайомство з основними видами сучасних ОС, короткий огляд їх можливостей.

## Матеріальне забезпечення занять:
1. ЕОМ типу IBM PC.
2. ОС сімейства Windows та віртуальна машина Virtual Box (Oracle).
3. ОС GNU/Linux (будь-який дистрибутив).
4. Сайт мережевої академії Cisco netacad.com та його онлайн курси по Linux

___

## Завдання для попередньої підготовки:

### __Словник термінів:__

- _Virtualization_ — віртуалізація; технологія створення логічної версії обчислювальних ресурсів (серверів, ОС, мереж, сховищ).
- _Virtual Machine_ (VM) — віртуальна машина; програмна імітація фізичного комп’ютера з власною операційною системою.
- _Virtual Environment_ — віртуальне середовище; ізольований програмний простір виконання.
- _Hypervisor_ — гіпервізор; програмний шар, що створює та керує віртуальними машинами.
- _Virtual Machine Monitor_ (VMM) — монітор віртуальних машин; синонім терміна «гіпервізор».
- _Type 1 Hypervisor_ (Bare-metal hypervisor) — гіпервізор типу 1; працює безпосередньо на апаратному забезпеченні без хост-ОС (наприклад, VMware ESXi).
- _Type 2 Hypervisor_ (Hosted hypervisor) — гіпервізор типу 2; працює поверх хост-операційної системи (наприклад, Oracle VM VirtualBox).
- _Host Operating System_ (Host OS) — хост-операційна система; основна ОС, у середовищі якої запускається гіпервізор типу 2.
- _Guest Operating System_ (Guest OS) — гостьова операційна система; ОС, встановлена всередині віртуальної машини.

### 2.1. __Охарактеризуйте поняття «гіпервізор». Які бувають їх типи?__
***A hypervisor*** (also called a Virtual Machine Monitor, VMM) is software that creates, runs, and manages virtual machines (VMs). It allocates physical resources (CPU, memory, storage, network) and ensures isolation between guest operating systems.

__There are two types of hypervisors:__ ⬇️
1. Type 1 Hypervisor (Bare-Metal Hypervisor) - runs directly on the physical hardware without a host operating system.
2. Type 2 Hypervisor (Hosted Hypervisor) - runs as an application on top of a host operating system.

___Main difference___
| Feature     | Type 1             | Type 2                       |
| ----------- | ------------------ | ---------------------------- |
| Runs on     | Hardware directly  | On host OS                   |
| Performance | Higher             | Slightly lower               |
| Typical use | Enterprise servers | Desktop testing, development |

### 2.2. __Перерахуйте основні компоненти та можливості гіпервізорів *VMware*__

