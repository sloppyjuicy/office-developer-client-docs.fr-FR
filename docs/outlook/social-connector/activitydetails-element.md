---
title: activityDetails, élément
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: L’élément activityDetails stocke les données brutes pour une seule activité de flux d’élément. Chaque activité flux élément doit avoir son propre élément activityDetails. Les données dans l’élément activityDetails sont référencées dans les modèles d’activité à l’aide des éléments de nom.
ms.openlocfilehash: c326017a038dff138d690b020a98972a08212690
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787579"
---
# <a name="activitydetails-element"></a>activityDetails, élément

L’élément **activityDetails** stocke les données brutes pour une seule activité de flux d’élément. Chaque activité flux élément doit avoir son propre élément **activityDetails** . Les données dans l’élément **activityDetails** sont référencées dans les modèles d’activité à l’aide des éléments de **nom** . Chaque élément de données dans l’élément **activityDetails** doit avoir un élément de **nom** . 
  
Le tableau suivant décrit les six éléments nécessitant l’élément **activityDetails** . 
  
|**Élément**|**Description**|
|:-----|:-----|
|**ownerID** <br/> |L’ID de l’utilisateur sur le réseau social qui a généré cette activité de flux d’élément.  <br/> |
|**objectID** <br/> |Une chaîne unique pour l’activité de flux de l’élément pour détecter les éléments d’alimentation en double.  <br/> |
|**applicationId** <br/> |Une des deux identificateurs uniques qui sont utilisés pour la correspondance de l’activité de flux élément avec son modèle. Si vous disposez de plusieurs applications ou autres groupes, il peut servir en tant qu’un organisateur de modèle de premier niveau.  <br/> |
|**templateId** <br/> |Le second ID unique qui est utilisé pour la correspondance de l’activité de flux élément avec son modèle. Cela peut servir d’un organisateur de modèle de second niveau.  <br/> |
|**date de publication** <br/> |La date et l’heure de l’activité de flux d’élément a été publié.  <br/> |
|**templateVariables** <br/> |Les données à utiliser dans les jetons de l’activité de flux de modèle d’élément.  <br/> |
   
Pour obtenir un exemple de l’activité de flux XML, voir [Exemple de code XML activité de flux](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du code XML pour une activité de flux d’élément](overview-of-xml-for-an-activity-feed-item.md)  
- [activityTemplateContainer, élément](activitytemplatecontainer-element.md)  
- [Variables de modèle](template-variables.md) 
- [Conseils pour l’affichage correctement les activités](guidelines-for-properly-displaying-activities.md)  
- [XML pour les activités](xml-for-activities.md)  
- [Fournisseur Outlook Social Connector schéma XML](outlook-social-connector-provider-xml-schema.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

