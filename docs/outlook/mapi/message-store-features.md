---
title: Fonctionnalités de la boutique de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d9167cd2-fc88-46b1-9a26-151955fb606c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f744924b260acbce5a97c8ee5bc58d434655705b
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770709"
---
# <a name="message-store-features"></a>Fonctionnalités de la boutique de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de magasins de messages sont plus complexes que les autres fournisseurs de services MAPI, car ils disposent d’un plus large éventail de fonctionnalités facultatives qu’ils peuvent implémenter. La liste des fonctionnalités requises pour un fournisseur de magasins de messages est relativement courte. Toutefois, un fournisseur de magasin de messages classique prendra en charge un certain nombre de fonctionnalités facultatives, car de nombreuses fonctionnalités facultatives sont très utiles ou requises par la plupart des clients MAPI. Le tableau suivant répertorie les principales fonctionnalités que les fournisseurs de magasins de messages peuvent implémenter et indique si chaque fonctionnalité est requise ou facultative pour tous les fournisseurs de magasins de messages et pour les fournisseurs de magasins de messages par défaut.
  
|**Fonctionnalité**|**All**|**Par défaut**|
|:-----|:-----|:-----|
|Fourniture de l’état avec la table d’état MAPI. |Obligatoire  <br/> |Obligatoire  <br/> |
|Mise en œuvre d’objets de dossier. |Obligatoire  <br/> |Obligatoire  <br/> |
|Mise en œuvre d’objets de message. |Obligatoire  <br/> |Obligatoire  <br/> |
|Fournir des rapports de lecture et nonread. |Obligatoire  <br/> |Obligatoire  <br/> |
|Fourniture d’une interface de progression. |Obligatoire  <br/> |Obligatoire  <br/> |
|Fourniture d’une interface de configuration. |Obligatoire  <br/> |Obligatoire  <br/> |
|Prise en charge des tables de contenu associées pour la prise en charge des formulaires et des affichages. |Facultatif  <br/> |Facultatif  <br/> |
|Envoi de messages avec le fournisseur de la boutique de messages. |Facultatif  <br/> |Requis  <br/> |
|Réception de messages avec le fournisseur de la boutique de messages. |Facultatif  <br/> |Requis  <br/> |
|Prise en charge des pièces jointes de message. |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge du format texte enrichi pour les messages. |Facultatif  <br/> |Facultatif  <br/> |
|Fourniture de notifications. |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge des recherches. |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge de fournisseurs de transport/magasin de messages étroitement couplés. |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge de la non-réutilisation des identificateurs d’entrée. |Facultatif  <br/> |Facultatif  <br/> |
   
Bon nombre des fonctionnalités facultatives peuvent être publiées dans MAPI et les applications clientes en paraxant différents indicateurs dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de l’objet de la boutique de messages. Les fonctionnalités requises ne sont pas associées à des indicateurs. **PR_STORE_SUPPORT_MASK** est requis sur les objets de message, de dossier et de message. 
  
## <a name="see-also"></a>Voir aussi



[Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

