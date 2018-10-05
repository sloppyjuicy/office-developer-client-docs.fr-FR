---
title: À propos des demandes de réunion en tant que mises à jour intégrales et mises à jour à caractère informatif
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 084928ca-efc0-36da-fe4f-5cc45f226178
description: Une demande de réunion est un message électronique qui a IPM. Schedule.Meeting.Request en tant que la classe de message. Par défaut, un participant reçoit une demande de réunion y répond directement.
ms.openlocfilehash: 8e7ab7a85d3f9f7c0a67245b8d8ad27442f5c5e4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400130"
---
# <a name="about-meeting-requests-as-informational-updates-and-full-updates"></a>À propos des demandes de réunion en tant que mises à jour intégrales et mises à jour à caractère informatif

Une demande de réunion est un message électronique qui a **IPM. Schedule.Meeting.Request** en tant que la classe de message. Par défaut, un participant reçoit une demande de réunion y répond directement. Outlook prend en charge la configuration de délégués qui peuvent répondre aux demandes de réunion pour le compte du destinataire principal. Outlook définit par programmation, la propriété nommée [PidLidMeetingType](https://msdn.microsoft.com/library/290b290c-7836-4a7e-bf1a-8d0225a07e56%28Office.15%29.aspx) une demande de réunion pour identifier l’état actuel de la mise à jour. 
  
## <a name="recipients-without-delegates"></a>Destinataires sans délégués

Lorsque Outlook reçoit une demande de réunion, les ensembles Outlook **mtgRequest**élément de la propriété **PidLidMeetingType** de la demande de réunion. Toute mise à jour de cette réunion est **mtgFullUpdate** (mise à jour intégrale) ou **mtgInfoUpdate** (mise à jour d’information) en fonction de la cause de la mise à jour avec Outlook définir **PidLidMeetingType** en conséquence. Une mise à jour complète requiert un participant explicitement répondre à la demande de réunion, et n’est pas le cas d’une mise à jour d’information. 
  
## <a name="full-updates"></a>Mises à jour complètes

Il existe deux scénarios de résultat dans une mise à jour complète :
  
- Lorsqu’un organisateur modifie la date, l’heure, fuseaux horaires ou la périodicité d’une demande de réunion précédente, l’organisateur doit envoyer une mise à jour à tous les participants. Cette mise à jour est une mise à jour complet auquel un participant doit répondre explicitement pour avertir l’organisateur de la présence, car Outlook ignore les réponses précédentes.
    
- Si un participant n’a pas répondu à une demande de réunion initiale et reçoit une mise à jour ultérieur, la demande de réunion initiale deviennent obsolète et la mise à jour est une mise à jour complète, quelle que soit la cause de la mise à jour.
    
## <a name="informational-updates"></a>Mises à jour d’information

Il existe quatre scénarios dans lesquels Outlook génère une mise à jour d’information. Dans ces scénarios, la réponse à la mise à jour d’information est facultative.
  
- Si un organisateur modifie l’emplacement d’une demande de réunion précédente, l’organisateur doit envoyer une mise à jour à tous les participants. Si un participant a déjà accepté la demande de réunion initiale, le participant reçoit la mise à jour sous la forme d’une mise à jour d’information.
    
- Si un organisateur ajoute un participant à une demande de réunion précédente, l’organisateur doit envoyer la demande de réunion sur le participant nouvellement ajouté et a la possibilité d’inclure les participants existants sur la mise à jour. Le participant nouvellement ajouté reçoit la demande de réunion en tant que nouvelle demande. Si l’organisateur choisit d’envoyer une mise à jour aux participants existants, les participants reçoivent la mise à jour comme une mise à jour d’information.
    
- Si un organisateur supprime un participant d’une demande de réunion précédente, l’organisateur doit envoyer une mise à jour sur le participant qui a été supprimé de la demande de réunion et dispose d’une option pour inclure les participants existants sur la mise à jour. Les participants recevront la mise à jour comme une mise à jour d’information.
    
- Si un organisateur modifie l’objet ou le corps d’une demande de réunion précédente, l’organisateur a la possibilité d’envoyer une mise à jour aux participants ou simplement enregistrer les modifications apportées à la copie de l’organisateur de la demande de réunion. Si l’organisateur choisit d’envoyer une mise à jour, les participants reçoivent la mise à jour comme une mise à jour d’information.
    
## <a name="recipients-set-up-with-delegates"></a>Destinataires configurée avec les délégués

Destinataires qui choisissent pour définir des délégués peuvent avoir des délégués répondre aux demandes de réunion que Private ne sont pas marqués. Par défaut, le principal reçoit uniquement une copie d’une demande de réunion ou une copie d’une mise à jour une demande de réunion précédente, et les délégués toujours recevoir la demande de réunion d’origine ou mise à jour de complète ou d’information d’origine. Dans cette configuration par défaut, le principal toujours reçoit les demandes de réunion déléguée et mises à jour ; les délégués du principal reçoivent des demandes de réunion en tant que nouvelles demandes de réunion, les mises à jour complètes ou les mises à jour d’information, comme indiqué pour les destinataires sans délégués dans la section « Destinataires sans délégués ».
  
Par défaut, les principaux permettre choisir répondre aux demandes de réunion non privés et les mises à jour, même si les délégués sont configurés pour eux. Toutefois, au lieu de cela, les administrateurs peuvent définir une stratégie pour empêcher les principaux destinataires de répondre.
  

