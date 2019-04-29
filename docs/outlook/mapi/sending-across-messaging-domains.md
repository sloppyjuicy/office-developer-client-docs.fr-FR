---
title: Envoi dans les domaines de messagerie
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
# <a name="sending-across-messaging-domains"></a>Envoi dans les domaines de messagerie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un domaine de messagerie représente un ou plusieurs systèmes de messagerie qui partagent un format d'adresse commun. La communication entre plusieurs domaines de messagerie implique la conversion d'un message envoyé au format du domaine de messagerie d'origine au format du domaine de messagerie de destination. Étant donné que tous les formats d'adresse ne sont pas compatibles, une passerelle est nécessaire pour convertir les informations d'adressage du format source au format de destination. Pour garantir la validité dans les domaines de messagerie, les applications clientes stockent des informations d'adressage importantes dans les propriétés MAPI. En outre, les passerelles effectuent la traduction, en examinant les propriétés dont il faut effectuer une traduction et en les modifiant selon un format que le domaine de messagerie de destination peut utiliser.
  
Auparavant, MAPI permettait d'associer ces informations d'adressage uniquement aux utilisateurs qui forment la liste de destinataires actuelle d'un message. Les propriétés décrivant chaque membre de la liste des destinataires ont subi la conversion requise par la passerelle afin de s'assurer de la validité des domaines de messagerie. Toutefois, certaines applications exigent que leurs messages incluent des informations d'adressage concernant les utilisateurs qui ont pu être des destinataires dans le passé, seront des destinataires à l'avenir ou ne recevront jamais de destinataires. Par exemple, les applications de routage, qui envoient des messages dans un ordre spécifique à un groupe d'utilisateurs, incorporent des informations d'adressage concernant ces utilisateurs dans les messages. Les informations incorporées incluent généralement l'adresse et le type d'adresse des destinataires à venir, ainsi que leurs rôles et positions dans l'ordre de routage, leur nom et un ou plusieurs identificateurs binaires par destinataire.
  
Pour permettre aux messages d'inclure des informations sur ces utilisateurs non destinataires, MAPI inclut désormais une stratégie permettant de s'assurer que les informations non relatives aux destinataires sont également traduites correctement dans les domaines de messagerie. Cette stratégie est basée sur le concept des propriétés mappées sur la passerelle.
  

