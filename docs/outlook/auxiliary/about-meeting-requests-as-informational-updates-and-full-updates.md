---
title: À propos des demandes de réunion en tant que mises à jour intégrales et mises à jour à caractère informatif
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 084928ca-efc0-36da-fe4f-5cc45f226178
description: Une demande de réunion est un e-mail avec IPM. Schedule.Meeting.Request en tant que classe de message. Par défaut, un participant qui reçoit une demande de réunion y répond directement.
ms.openlocfilehash: d6e138fb4639a590e31e5f797ff3604c050c6292
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605469"
---
# <a name="about-meeting-requests-as-informational-updates-and-full-updates"></a>À propos des demandes de réunion en tant que mises à jour intégrales et mises à jour à caractère informatif

Une demande de réunion est un e-mail avec **IPM. Schedule.Meeting.Request en** tant que classe de message. Par défaut, un participant qui reçoit une demande de réunion y répond directement. Outlook prend en charge la configuration des délégués qui peuvent répondre aux demandes de réunion au nom du destinataire principal. Par programme, Outlook définit la propriété nommée [PidLidMeetingType](https://msdn.microsoft.com/library/290b290c-7836-4a7e-bf1a-8d0225a07e56%28Office.15%29.aspx) d’une demande de réunion pour identifier l’état de mise à jour actuel. 
  
## <a name="recipients-without-delegates"></a>Destinataires sans délégués

Lorsque Outlook reçoit une nouvelle demande de réunion, Outlook la propriété **PidLidMeetingType** de l’élément de demande de réunion **sur mtgRequest**. Toute mise à jour ultérieure de cette réunion est **mtgFullUpdate** (mise à jour complète) ou **mtgInfoUpdate** (mise à jour d’informations) en fonction de la cause de la mise à jour, avec Outlook définir **PidLidMeetingType** en conséquence. Une mise à jour complète nécessite qu’un participant réponde explicitement à la demande de réunion, ce qui n’est pas le cas d’une mise à jour d’informations. 
  
## <a name="full-updates"></a>Mises à jour complètes

Deux scénarios entraînent une mise à jour complète :
  
- Lorsqu’un organisateur modifie la date, l’heure, les fuseaux horaires ou la récurrence d’une demande de réunion précédente, il doit envoyer une mise à jour à tous les participants. Cette mise à jour est une mise à jour complète à laquelle un participant doit répondre explicitement pour informer l’organisateur de la présence, Outlook ignore les réponses précédentes.
    
- Si un participant n’a pas répondu à une demande de réunion initiale et reçoit une mise à jour ultérieure, la demande de réunion initiale devient hors date et la mise à jour est une mise à jour complète, quelle que soit la cause de la mise à jour.
    
## <a name="informational-updates"></a>Mises à jour d’informations

Il existe quatre scénarios dans lesquels Outlook génère une mise à jour d’informations. Dans ces scénarios, la réponse à la mise à jour d’information est facultative.
  
- Si un organisateur modifie l’emplacement d’une demande de réunion précédente, il doit envoyer une mise à jour à tous les participants. Si un participant a déjà accepté la demande de réunion initiale, il reçoit la mise à jour en tant que mise à jour d’informations.
    
- Si un organisateur ajoute un participant à une demande de réunion précédente, il doit envoyer la demande de réunion au participant nouvellement ajouté et peut inclure des participants existants dans la mise à jour. Le participant nouvellement ajouté reçoit la demande de réunion en tant que nouvelle demande. Si l’organisateur choisit d’envoyer une mise à jour aux participants existants, ils reçoivent la mise à jour en tant que mise à jour d’informations.
    
- Si un organisateur supprime un participant d’une demande de réunion précédente, il doit envoyer une mise à jour au participant qui a été supprimé de la demande de réunion et peut inclure des participants existants dans la mise à jour. Les participants reçoivent la mise à jour en tant que mise à jour d’informations.
    
- Si un organisateur modifie l’objet ou le corps d’une demande de réunion précédente, il a la possibilité d’envoyer une mise à jour aux participants ou simplement d’enregistrer les modifications dans la copie de la demande de réunion de l’organisateur. Si l’organisateur choisit d’envoyer une mise à jour, les participants la reçoivent en tant que mise à jour d’informations.
    
## <a name="recipients-set-up-with-delegates"></a>Destinataires à configurer avec des délégués

Les destinataires qui choisissent de configurer des délégués peuvent avoir des délégués qui répondent aux demandes de réunion qui ne sont pas marquées comme privées. Par défaut, le principal reçoit uniquement une copie d’une demande de réunion ou une copie d’une mise à jour d’une demande de réunion précédente, et les délégués reçoivent toujours la demande de réunion d’origine ou la mise à jour complète ou d’information d’origine. Dans cette configuration par défaut, le principal reçoit toujours les demandes de réunion déléguées et les mises à jour . les délégués du principal reçoivent les demandes de réunion sous forme de nouvelles demandes de réunion, de mises à jour complètes ou de mises à jour d’informations, comme décrit pour les destinataires sans délégués dans la section « Destinataires sans délégués ».
  
Par défaut, les principaux peuvent choisir de répondre aux demandes et mises à jour de réunion non privées, même si les délégués sont configurer pour le faire en leur nom. Toutefois, en remplacement, les administrateurs peuvent configurer une stratégie pour empêcher les destinataires principaux de répondre.
  

