---
title: Rendez-vous
TOCTitle: Appointments
ms:assetid: 989a94a8-c1dc-4c5d-ab2b-2cc29a08f8a3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184627(v=office.15)
ms:contentKeyID: 55119805
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 932dc7c4661d34c2922814142c1b0b67527e8cb7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549755"
---
# <a name="appointments"></a>Rendez-vous

Cette section fournit des exemples de tâches qui mettent en œuvre des rendez-vous. Le terme « rendez-vous » fait notamment référence aux événements, réunions et rendez-vous périodiques. Outlook utilise l’objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) pour représenter les rendez-vous dans le dossier Calendrier.

## <a name="in-this-section"></a>Dans cette section

|Rubrique|Description|
|:----|:----------|
|[Création d’un rendez-vous sur toute la journée](how-to-create-an-appointment-that-is-an-all-day-event.md)  |Utilise la propriété [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) pour créer un rendez-vous qui est un événement planifié sur une journée entière.|
|[Création d’un rendez-vous qui commence dans le fuseau horaire Pacifique et se termine dans le fuseau horaire Est](how-to-create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone.md)  |Crée un rendez-vous qui commence dans le fuseau horaire Pacifique (UTC-8) et se termine dans le fuseau horaire Est (UTC-5)|
|[Spécifier les différents types de destinataires d’un élément de rendez-vous](how-to-specify-different-recipient-types-for-an-appointment-item.md)  |Utilise l’énumération [OlMeetingRecipientType](https://msdn.microsoft.com/library/bb623431\(v=office.15\)) pour spécifier différents types de destinataires pour un élément de rendez-vous.|
|[Création d’un rendez-vous périodique selon une périodicité par défaut](how-to-create-a-recurring-appointment-by-using-the-default-recurrence-pattern.md)  |Crée un rendez-vous périodique selon une périodicité par défaut.|
|[Création d’un rendez-vous périodique selon une périodicité hebdomadaire](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md)  |Crée un rendez-vous périodique ayant une périodicité hebdomadaire (par exemple, un rendez-vous qui a lieu chaque lundi, mercredi et vendredi).|
|[Création d’un rendez-vous périodique annuel selon une périodicité toutes les n années](how-to-create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern.md)  |Crée un rendez-vous dont la périodicité annuelle est un jour spécifique. Par exemple, le premier lundi du mois de juin.|
|[Trouver un rendez-vous spécifique dans une série de rendez-vous périodiques](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md)  |Montre comment renvoyer un objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) qui représente un rendez-vous spécifique dans une série de rendez-vous périodiques.|
|[Créer une exception de rendez-vous dans une série de rendez-vous périodiques](how-to-create-an-exception-appointment-in-a-recurring-appointment-series.md)  |Utilise un objet [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) pour créer une exception à la périodicité standard d’un rendez-vous.|
|[Création d’un rappel pour un élément de rendez-vous](how-to-create-a-reminder-for-an-appointment-item.md)  |Utilise la propriété [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) pour créer un rappel pour un élément de rendez-vous.|
|[Importation des données XML de rendez-vous dans les objets de rendez-vous Outlook](how-to-import-appointment-xml-data-into-outlook-appointment-objects.md)  |Lit des données de rendez-vous au format XML, enregistre les données dans des objets AppointmentItem d'Outlook dans le calendrier par défaut et retourne les objets de rendez-vous dans un tableau.|

## <a name="see-also"></a>Voir aussi

- [Calendrier](calendar.md)
- [Demandes de réunion](meeting-requests.md)
- [Procédure (Référence PIA Outlook 2013)](how-do-i-outlook-2013-pia-reference.md)

