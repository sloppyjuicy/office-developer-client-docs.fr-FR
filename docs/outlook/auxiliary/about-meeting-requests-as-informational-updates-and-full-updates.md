---
title: À propos des demandes de réunion en tant que mises à jour intégrales et mises à jour à caractère informatif
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 084928ca-efc0-36da-fe4f-5cc45f226178
description: Une demande de réunion est un courrier électronique qui contient IPM. Schedule. Meeting. Request en tant que classe de message. Par défaut, un participant qui reçoit une demande de réunion y répond directement.
ms.openlocfilehash: 8e7ab7a85d3f9f7c0a67245b8d8ad27442f5c5e4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316995"
---
# <a name="about-meeting-requests-as-informational-updates-and-full-updates"></a>À propos des demandes de réunion en tant que mises à jour intégrales et mises à jour à caractère informatif

Une demande de réunion est un courrier électronique qui contient **IPM. Schedule. Meeting. Request** en tant que classe de message. Par défaut, un participant qui reçoit une demande de réunion y répond directement. Outlook prend en charge la configuration des délégués qui peuvent répondre aux demandes de réunion pour le compte du destinataire principal. Par programme, Outlook définit la propriété nommée [PidLidMeetingType](https://msdn.microsoft.com/library/290b290c-7836-4a7e-bf1a-8d0225a07e56%28Office.15%29.aspx) d'une demande de réunion pour identifier l'état de mise à jour actuel. 
  
## <a name="recipients-without-delegates"></a>Destinataires sans délégués

Quand Outlook reçoit une nouvelle demande de réunion, Outlook définit la propriété **PidLidMeetingType** de l'élément de demande de réunion sur **mtgRequest**. Toute mise à jour ultérieure de cette réunion est soit **mtgFullUpdate** (mise à jour complète), soit **mtgInfoUpdate** (mise à jour informatif) en fonction de la cause de la mise à jour, avec le paramètre **PidLidMeetingType** en conséquence. Une mise à jour complète nécessite qu'un participant réponde explicitement à la demande de réunion et qu'aucune mise à jour n'existe. 
  
## <a name="full-updates"></a>Mises à jour intégrales

Il existe deux scénarios qui entraînent une mise à jour complète:
  
- Lorsqu'un organisateur modifie la date, l'heure, les fuseaux horaires ou la périodicité d'une demande de réunion précédente, l'organisateur doit envoyer une mise à jour à tous les participants. Cette mise à jour est une mise à jour complète à laquelle un participant doit répondre explicitement pour avertir l'organisateur de la participation, car Outlook ignore les réponses précédentes.
    
- Si un participant n'a pas répondu à une demande de réunion initiale et reçoit une mise à jour ultérieure, la demande de réunion initiale devient obsolète et la mise à jour est une mise à jour complète, quelle que soit la cause de la mise à jour.
    
## <a name="informational-updates"></a>Mises à jour d'information

Il existe quatre scénarios dans lesquels Outlook génère une mise à jour des informations. Dans ces scénarios, la réponse à la mise à jour informatif est facultative.
  
- Si un organisateur modifie l'emplacement d'une demande de réunion précédente, l'organisateur doit envoyer une mise à jour à tous les participants. Si un participant a déjà accepté la demande de réunion initiale, le participant reçoit la mise à jour sous la forme d'une mise à jour informatif.
    
- Si un organisateur ajoute un participant à une demande de réunion précédente, l'organisateur doit envoyer la demande de réunion au participant nouvellement ajouté et peut inclure des participants existants sur la mise à jour. Le participant nouvellement ajouté reçoit la demande de réunion en tant que nouvelle demande. Si l'organisateur choisit d'envoyer une mise à jour aux participants existants, les participants reçoivent la mise à jour sous la forme d'une mise à jour.
    
- Si un organisateur supprime un participant d'une demande de réunion précédente, l'organisateur doit envoyer une mise à jour au participant qui a été supprimé de la demande de réunion et peut inclure des participants existants sur la mise à jour. Les participants reçoivent la mise à jour sous la forme d'une mise à jour informatif.
    
- Si un organisateur modifie l'objet ou le corps d'une demande de réunion précédente, l'organisateur a la possibilité d'envoyer une mise à jour aux participants ou simplement d'enregistrer les modifications apportées à la copie de réunion de l'organisateur. Si l'organisateur choisit d'envoyer une mise à jour, les participants reçoivent la mise à jour sous la forme d'une mise à jour informatif.
    
## <a name="recipients-set-up-with-delegates"></a>Destinataires configurés avec des délégués

Les destinataires qui choisissent de configurer des délégués peuvent répondre à des demandes de réunion qui ne sont pas marquées comme privées. Par défaut, le principal reçoit uniquement une copie d'une demande de réunion ou d'une copie d'une mise à jour d'une demande de réunion précédente, et les délégués reçoivent toujours la demande de réunion d'origine ou la mise à jour complète ou informatif originale. Dans cette configuration par défaut, le principal reçoit toujours les demandes de réunion déléguées et les mises à jour; les délégués du principal reçoivent des demandes de réunion en tant que nouvelles demandes de réunion, mises à jour intégrales ou mises à jour d'information, comme indiqué pour les destinataires sans délégués dans la section «destinataires sans délégués».
  
Par défaut, les principaux peuvent choisir de répondre aux demandes de réunion et aux mises à jour non privées, même si les délégués sont configurés pour le faire pour leur compte. Toutefois, les administrateurs peuvent configurer une stratégie pour empêcher les destinataires principaux de répondre.
  

