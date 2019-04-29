---
title: Interfaces de fournisseur Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (OSC) est une fonctionnalité Office partagée par les applications clientes Office qui se connecte aux réseaux sociaux et d'entreprise afin que les utilisateurs puissent rester en contact avec les personnes de leurs réseaux sans quitter Office.
ms.openlocfilehash: 77759db34f63239473e0682cfaca720860e96768
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422809"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Interfaces de fournisseur Outlook Social Connector

Outlook Social Connector (OSC) est une fonctionnalité Office partagée par les applications clientes Office qui se connecte aux réseaux sociaux et d'entreprise afin que les utilisateurs puissent rester en contact avec les personnes de leurs réseaux sans quitter Office. 
  
Un fournisseur OSC est une DLL COM (Component Object Model) qui permet à l'objet OSC d'accéder aux données de réseau social d'une manière indépendante des API de chaque réseau social. Le tableau suivant répertorie les interfaces dans l'extensibilité du fournisseur OSC. Un fournisseur OSC doit implémenter quatre des cinq interfaces pour communiquer avec OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)et [ISocialSession](isocialsessioniunknown.md). Si le fournisseur OSC prend en charge les activités de synchronisation, la synchronisation à la demande ou hybride des amis, la mise en cache des informations d'identification d'ouverture de session et la connexion à l'aide des informations d'identification mises en cache, ou la possibilité de suivre une personne, le fournisseur doit implémenter [ISocialSession2 ](isocialsession2iunknown.md).
  
|**Nom**|**Description**|
|:-----|:-----|
|[ISocialPerson](isocialpersoniunknown.md) <br/> |Représente une personne sur le réseau social.  <br/> |
|[ISocialProfile](isocialprofileisocialperson.md) <br/> |Représente l'utilisateur connecté.  <br/> |
|[ISocialProvider](isocialprovideriunknown.md) <br/> |Représente une instance d'un fournisseur OSC.  <br/> |
|[ISocialSession](isocialsessioniunknown.md) <br/> |Représente une connexion à un site de réseau social.  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |Prend en charge les activités de synchronisation, l'ajout de amis, la synchronisation à la demande ou hybride des amis, ou la connexion au réseau social à l'aide des informations d'identification mises en cache.  <br/> |
   

