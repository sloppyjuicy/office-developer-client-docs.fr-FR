---
title: Interfaces de fournisseur Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: L’Outlook Social Connector (OSC) est une fonctionnalité Office partagée par les applications clientes Office qui se connecte à la mise en réseau et réseaux d’entreprise afin que les utilisateurs peuvent rester en contact avec les personnes figurant dans leurs réseaux sans quitter Office.
ms.openlocfilehash: bc393f32e563bbbef70538ea00cd92cf7f96729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787702"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Interfaces de fournisseur Outlook Social Connector

L’Outlook Social Connector (OSC) est une fonctionnalité Office partagée par les applications clientes Office qui se connecte à la mise en réseau et réseaux d’entreprise afin que les utilisateurs peuvent rester en contact avec les personnes figurant dans leurs réseaux sans quitter Office. 
  
Un fournisseur OSC est un composant COM (Object Model) DLL qui permet à l’OSC accéder aux données de réseau social de façon indépendante des API de chaque réseau social. Le tableau suivant répertorie les interfaces de l’extensibilité de fournisseur OSC. Un fournisseur OSC doit implémenter quatre des cinq interfaces pour communiquer avec l’OSC : [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)et [ISocialSession](isocialsessioniunknown.md). Si le fournisseur OSC prend en charge les activités de synchronisation, à la demande ou la synchronisation hybride d’amis, la mise en cache des informations d’identification d’ouverture de session et l’ouverture de session à l’aide de mis en cache les informations d’identification, ou la possibilité de suivre une personne, le fournisseur doit implémenter [ISocialSession2 ](isocialsession2iunknown.md), ainsi que.
  
|**Nom**|**Description**|
|:-----|:-----|
|[ISocialPerson](isocialpersoniunknown.md) <br/> |Représente une personne sur le réseau social.  <br/> |
|[ISocialProfile](isocialprofileisocialperson.md) <br/> |Représente l’utilisateur connecté.  <br/> |
|[ISocialProvider](isocialprovideriunknown.md) <br/> |Représente une instance d’un fournisseur OSC.  <br/> |
|[ISocialSession](isocialsessioniunknown.md) <br/> |Représente une connexion à un site de réseau social.  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |Prend en charge la synchronisation des activités, ajout de contacts, de la synchronisation de la demande ou hybride d’amis ou ouvrant une session sur le réseau social à l’aide de mises en cache les informations d’identification.  <br/> |
   

