---
title: Outlook interfaces de fournisseur Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (OSC) est une fonctionnalité de Office partagée par les applications clientes Office qui se connecte aux réseaux sociaux et professionnels afin que les utilisateurs restent en contact avec les personnes de leurs réseaux sans quitter Office.
ms.openlocfilehash: 9e640744fe2acdb4a85a349783fc5a2f080231fc
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62778754"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Outlook interfaces de fournisseur Social Connector

Outlook Social Connector (OSC) est une fonctionnalité de Office partagée par les applications clientes Office qui se connecte aux réseaux sociaux et professionnels afin que les utilisateurs restent en contact avec les personnes de leurs réseaux sans quitter Office. 
  
Un fournisseur OSC est une DLL COM (Component Object Model) qui permet à l’OSC d’accéder aux données de réseau social d’une manière indépendante des API de chaque réseau social. Le tableau suivant répertorie les interfaces dans l’extensibilité du fournisseur OSC. Un fournisseur OSC doit implémenter quatre des cinq interfaces pour communiquer avec l’OSC : [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md) et [ISocialSession](isocialsessioniunknown.md). Si le fournisseur OSC prend en charge la synchronisation des activités, la synchronisation à la demande ou hybride des amis, la mise en cache des informations d’identification de connexion et la connexion à l’aide des informations d’identification mises en cache, ou la possibilité de suivre une personne, le fournisseur doit également implémenter [ISocialSession2](isocialsession2iunknown.md).
  
|**Name**|**Description**|
|:-----|:-----|
|[ISocialPerson](isocialpersoniunknown.md) <br/> |Représente une personne sur le réseau social. |
|[ISocialProfile](isocialprofileisocialperson.md) <br/> |Représente l’utilisateur connecté. |
|[ISocialProvider](isocialprovideriunknown.md) <br/> |Représente une instance d’un fournisseur OSC. |
|[ISocialSession](isocialsessioniunknown.md) <br/> |Représente une connexion à un site de réseau social. |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |Prend en charge la synchronisation des activités, l’ajout d’amis, la synchronisation à la demande ou hybride d’amis, ou la connexion au réseau social à l’aide d’informations d’identification mises en cache. |
   

