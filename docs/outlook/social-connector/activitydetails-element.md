---
title: activityDetails, élément
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: L’élément activityDetails stocke les données brutes pour un seul élément de flux d’activités. Chaque élément de flux d’activités doit avoir son propre élément activityDetails. Les données de l’élément activityDetails sont référencés dans les modèles d’activité à l’aide d’éléments de nom.
ms.openlocfilehash: 6fc2e3cc9ded498eb2f976637bdd6929d9d368e9
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62782535"
---
# <a name="activitydetails-element"></a>activityDetails, élément

**L’élément activityDetails** stocke les données brutes pour un seul élément de flux d’activités. Chaque élément de flux d’activités doit avoir son propre **élément activityDetails** . Les données de **l’élément activityDetails sont référencés** dans les modèles d’activité à l’aide **d’éléments de** nom. Chaque élément de données dans **l’élément activityDetails** doit avoir un **élément** name. 
  
Le tableau suivant décrit les six éléments nécessaires à **l’élément activityDetails** . 
  
|**Élément**|**Description**|
|:-----|:-----|
|**ownerID** <br/> |ID de l’utilisateur sur le réseau social qui a généré cet élément de flux d’activités. |
|**objectID** <br/> |Chaîne unique pour l’élément de flux d’activités afin de détecter les éléments de flux en double. |
|**applicationId** <br/> |L’un des deux ID uniques utilisés pour faire correspondre l’élément de flux d’activités à son modèle. Si vous avez plusieurs applications ou d’autres regroupements, vous pouvez l’utiliser comme organisateur de modèles de premier niveau. |
|**templateId** <br/> |Deuxième ID unique utilisé pour faire correspondre l’élément de flux d’activités à son modèle. Il peut être utilisé en tant qu’organisateur de modèles de second niveau. |
|**publishDate** <br/> |Date et heure de publication de l’élément de flux d’activités. |
|**templateVariables** <br/> |Données à utiliser dans les jetons pour le modèle d’élément de flux d’activités. |
   
Pour obtenir un exemple de données XML de flux d’activités, voir [l’exemple XML des flux d’activités](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du XML pour un élément de flux d’activités](overview-of-xml-for-an-activity-feed-item.md)  
- [activityTemplateContainer, élément](activitytemplatecontainer-element.md)  
- [Variables de modèle](template-variables.md) 
- [Recommandations en matière d’affichage correct des activités](guidelines-for-properly-displaying-activities.md)  
- [XML pour les activités](xml-for-activities.md)  
- [Outlook schéma XML du fournisseur Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

