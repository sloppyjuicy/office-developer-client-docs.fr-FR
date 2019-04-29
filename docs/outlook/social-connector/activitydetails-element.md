---
title: Élément activityDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: L'élément activityDetails stocke les données brutes pour un élément de flux d'activité unique. Chaque élément de flux d'activité doit disposer de son propre élément activityDetails. Les données de l'élément activityDetails sont référencées dans les modèles d'activité à l'aide d'éléments Name.
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434871"
---
# <a name="activitydetails-element"></a>Élément activityDetails

L'élément **activityDetails** stocke les données brutes pour un élément de flux d'activité unique. Chaque élément de flux d'activité doit disposer de son propre élément **activityDetails** . Les données de l'élément **activityDetails** sont référencées dans les modèles d'activité à l'aide d'éléments **Name** . Chaque élément de données dans l'élément **activityDetails** doit avoir un élément **Name** . 
  
Le tableau suivant décrit les six éléments requis par l'élément **activityDetails** . 
  
|**Élément**|**Description**|
|:-----|:-----|
|**ownerID** <br/> |ID de l'utilisateur sur le réseau social qui a généré cet élément de flux d'activité.  <br/> |
|**objectID** <br/> |Une chaîne unique pour l'élément de flux d'activités afin de détecter les éléments de flux en double.  <br/> |
|**applicationId** <br/> |Un des deux ID uniques qui sont utilisés pour faire correspondre l'élément de flux d'activités avec son modèle. Si vous avez plusieurs applications ou autres groupements, il peut être utilisé en tant qu'organisateur de modèles de premier niveau.  <br/> |
|**templateId** <br/> |Deuxième ID unique utilisé pour faire correspondre l'élément de flux d'activités avec son modèle. Il peut être utilisé en tant qu'organisateur de modèles de second niveau.  <br/> |
|**publishDate** <br/> |Date et heure de publication de l'élément de flux d'activités.  <br/> |
|**templateVariables** <br/> |Les données à utiliser dans les jetons pour le modèle d'élément de flux d'activités.  <br/> |
   
Pour obtenir un exemple de XML d'informations sur les activités, voir [exemple de XML de flux d'activités](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble du code XML pour un élément de flux d'activité](overview-of-xml-for-an-activity-feed-item.md)  
- [Élément activityTemplateContainer](activitytemplatecontainer-element.md)  
- [Variables de modèle](template-variables.md) 
- [Instructions pour afficher correctement les activités](guidelines-for-properly-displaying-activities.md)  
- [XML pour les activités](xml-for-activities.md)  
- [Schéma XML du fournisseur Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

