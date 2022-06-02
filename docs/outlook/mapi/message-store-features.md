---
title: Fonctionnalités du Magasin de messages
description: Décrit les principales fonctionnalités que les fournisseurs de magasins de messages peuvent implémenter et indique si chaque fonctionnalité est requise ou facultative pour certains fournisseurs de magasins.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d9167cd2-fc88-46b1-9a26-151955fb606c
ms.openlocfilehash: 54ff07d82c345809e69361407ab950983a84df94
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828100"
---
# <a name="message-store-features"></a>Fonctionnalités du Magasin de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de magasins de messages sont plus complexes que d’autres fournisseurs de services MAPI dans le sens où les fournisseurs de magasins de messages disposent d’un plus large éventail de fonctionnalités facultatives qu’ils peuvent implémenter. La liste des fonctionnalités requises pour un fournisseur de magasin de messages est assez courte. Toutefois, un fournisseur de magasin de messages classique prend en charge un certain nombre de fonctionnalités facultatives, car la plupart des fonctionnalités facultatives sont très utiles ou requises par la plupart des clients MAPI. Le tableau suivant répertorie les principales fonctionnalités que les fournisseurs de magasin de messages peuvent implémenter et indique si chaque fonctionnalité est requise ou facultative pour tous les fournisseurs de magasins de messages et pour les fournisseurs de magasins de messages par défaut.
  
|**Fonctionnalité**|**All**|**Par défaut**|
|:-----|:-----|:-----|
|Fourniture de l’état avec la table d’état MAPI. |Obligatoire  <br/> |Obligatoire  <br/> |
|Implémentation d’objets de dossier. |Obligatoire  <br/> |Obligatoire  <br/> |
|Implémentation d’objets de message. |Obligatoire  <br/> |Obligatoire  <br/> |
|Fournir des rapports de lecture et nonread. |Obligatoire  <br/> |Obligatoire  <br/> |
|Fourniture d’une interface de progression. |Obligatoire  <br/> |Obligatoire  <br/> |
|Fourniture d’une interface de configuration. |Obligatoire  <br/> |Obligatoire  <br/> |
|Prise en charge des tables de contenu associées pour la prise en charge des formulaires et des affichages. |Facultatif  <br/> |Facultatif  <br/> |
|Envoi de messages avec le fournisseur du magasin de messages. |Facultatif  <br/> |Requis  <br/> |
|Réception de messages avec le fournisseur du magasin de messages. |Facultatif  <br/> |Requis  <br/> |
|Prise en charge des pièces jointes de message. |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge du format de texte enrichi pour les messages. |Facultatif  <br/> |Facultatif  <br/> |
|Envoi de notifications. |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge des recherches. |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge des fournisseurs de stockage/transport de messages étroitement couplés. |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge de la non-réutilisation des identificateurs d’entrée. |Facultatif  <br/> |Facultatif  <br/> |
   
La plupart des fonctionnalités facultatives peuvent être publiées sur MAPI et les applications clientes en définissant différents indicateurs dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de l’objet du magasin de messages. Les fonctionnalités requises n’ont pas d’indicateurs associés. **PR_STORE_SUPPORT_MASK** est nécessaire sur le magasin de messages, le dossier et les objets de message. 
  
## <a name="see-also"></a>Voir aussi



[Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

