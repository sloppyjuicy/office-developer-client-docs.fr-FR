---
title: Envoi sur des domaines de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 65594253-66cd-486a-aa5b-0bc719f761f0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 40c12a4010d51cb433b62558b5fe1d12afb583dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567068"
---
# <a name="sending-across-messaging-domains"></a>Envoi sur des domaines de messagerie

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un domaine de messagerie représente un ou plusieurs systèmes de messagerie qui partagent un même format d’adresse. Communication entre plusieurs domaines de messagerie implique la traduction d’un message envoyé dans le format du domaine de messagerie d’origine dans le format du domaine de messagerie de destination. Pas tous les formats d’adresse sont compatibles, une passerelle est nécessaire pour traduire les informations d’adressage du format source dans le format de destination. Pour garantir la validité sur plusieurs domaines de messagerie, les applications clientes stockent des informations d’adressage importantes dans les propriétés MAPI. En outre, les passerelles effectuent la traduction en examinant les propriétés connus traduction et de les modifier dans un format utilisable par le domaine de messagerie de destination.
  
Auparavant, MAPI autorisés ces informations d’adressage à associer uniquement les utilisateurs qui composent la liste des destinataires d’un message en cours. Les propriétés de chaque membre de la liste des destinataires a subi la traduction requise par la passerelle pour garantir la validité sur plusieurs domaines de messagerie. Cependant, certaines applications nécessitent que leurs messages incluent des informations sur les utilisateurs qui ont peut-être des destinataires dans le passé d’adressage, seront à l’avenir destinataires ou ne sera jamais destinataires. Par exemple, des applications de routage qui envoient les messages à un groupe d’utilisateurs dans l’ordre indiqué, incorporent adressage d’informations sur ces utilisateurs dans les messages. Les informations incorporées incluent généralement l’adresse et le type d’adresse des destinataires futures et peut-être également leurs rôles et position dans l’ordre de routage, leurs noms et un ou plusieurs identificateurs binaires par destinataire.
  
Pour autoriser les messages à inclure des informations sur ces utilisateurs nonrecipient, MAPI inclut désormais une stratégie pour s’assurer que ces informations nonrecipient sont également traduites correctement entre les domaines de messagerie. Cette stratégie est basée sur le concept des propriétés mappables-passerelle.
  

