---
title: Envoi entre domaines de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 65594253-66cd-486a-aa5b-0bc719f761f0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ddbaa4aeacf17f2c266ccc0ff963d005f9e403ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410111"
---
# <a name="sending-across-messaging-domains"></a>Envoi entre domaines de messagerie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un domaine de messagerie représente un ou plusieurs systèmes de messagerie qui partagent un format d’adresse commun. La communication entre plusieurs domaines de messagerie implique la traduction d’un message envoyé au format du domaine de messagerie d’origine au format du domaine de messagerie de destination. Étant donné que tous les formats d’adresse ne sont pas compatibles, une passerelle est nécessaire pour traduire les informations d’adressan du format source au format de destination. Pour garantir la validité entre les domaines de messagerie, les applications clientes stockent des informations d’adressa ment importantes dans les propriétés MAPI. En outre, les passerelles effectuent la traduction, en examinant les propriétés connues pour avoir besoin d’une traduction et en les modifiant dans un format que le domaine de messagerie de destination peut utiliser.
  
Auparavant, MAPI permettait l’associer uniquement aux utilisateurs qui composent la liste des destinataires actuels d’un message. Les propriétés décrivant chaque membre de la liste des destinataires décrivent la traduction requise par la passerelle pour garantir la validité entre les domaines de messagerie. Toutefois, certaines applications exigent que leurs messages incluent des informations sur les utilisateurs qui étaient peut-être des destinataires dans le passé, qui seront des destinataires à l’avenir ou qui ne seront jamais des destinataires. Par exemple, les applications de routage, qui envoient des messages dans un ordre spécifié à un groupe d’utilisateurs, incorporent les informations d’adressage de ces utilisateurs dans les messages. Les informations incorporées incluent généralement l’adresse et le type d’adresse des futurs destinataires, et éventuellement leurs rôles et positions dans l’ordre de routage, leurs noms et un ou plusieurs identificateurs binaires par destinataire.
  
Pour permettre aux messages d’inclure des informations sur ces utilisateurs noncipients, MAPI inclut désormais une stratégie permettant de s’assurer que ces informations noncipientes sont également traduites correctement sur les domaines de messagerie. Cette stratégie est basée sur le concept de propriétés de passerelle mappables.
  

