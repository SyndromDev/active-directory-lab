# Active Directory Home Lab

## Обзор
Этот проект демонстрирует развертывание и настройку базовой среды Active Directory с использованием Windows Server.

Целью проекта было моделирование инфраструктуры небольшой компании с доменными службами, DNS и организацией пользователей.

## Обзор архитектуры
Клиент → DNS → Контроллер домена → Active Directory

---

## Окружение
- Windows Server (контроллер домена)
- VirtualBox / VMware
- Windows 11 (клиент — опционально)

---

## Информация о домене
- Имя домена: **company.local**
- Контроллер домена: **DC-01**

---

## Настроенные компоненты

### Active Directory
- Установлены службы Active Directory Domain Services (AD DS)
- Сервер повышен до роли контроллера домена

### DNS
- Настроен DNS-сервер на контроллере домена
- Создана зона прямого просмотра: `company.local`
- Проверено разрешение доменных имен

### Организационная структура
- Созданы Organizational Units (OU):
  - IT
  - HR
  - Users
- Созданы учетные записи пользователей домена

---

## Проверка работоспособности

Тест разрешения DNS:

- nslookup company.local

Ожидаемый результат:
- Возвращается IP-адрес контроллера домена

---

## Group Policy (GPO)

В домене были применены базовые настройки групповых политик:

- Настройка политики паролей
- Политика блокировки учетных записей
- Изменения стандартной доменной политики

Эти политики обеспечивают базовое усиление безопасности среды.

---

## Схема IP-адресации

| Device        | IP Address       | Role                |
|--------------|-----------------|--------------------|
| DC-01        | 192.168.31.250  | Domain Controller   |
| Windows 11   | 192.168.31.10   | Client Machine      |
| Gateway      | 192.168.31.1    | Network Gateway     |

Маска подсети: 255.255.255.0  
DNS-сервер: 192.168.31.250

---

## Скриншоты

### Структура Active Directory
![AD Structure](screenshots/structure.png)

### Пользователи в Organizational Units
![Users](screenshots/ActiveDirectory.png)

### Пользователи в IT (Helpdesk)
![Helpdesk](screenshots/helpdesk.png)

### Пользователи в IT (Администраторы)
![Admins](screenshots/SysAdmins.png)

### Пользователи в Employees
![Employees](screenshots/Users.png)

### Настройка DNS
![DNS](screenshots/DNSmanager.png)

### company.local
![Company local](screenshots/companylocal.png)

### Тест разрешения домена
![NSLookup](screenshots/Name.png)

### Сервер-клиент
![Server-client](screenshots/Server-client.png)

##  Схема сети
Диаграмма ниже показывает архитектуру лабораторной сети.
![Diagram](screenshots/network_diagram.png)

---

## Примечания
Подключение клиентской машины к домену не было завершено из-за ограничений редакции Windows Home.

---

## Результат
Была успешно развернута рабочая среда Active Directory с DNS и организационной структурой, имитирующей инфраструктуру реальной компании.
