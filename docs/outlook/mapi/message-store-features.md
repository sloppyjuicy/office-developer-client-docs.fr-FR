---
title: Fonctionnalités de la boutique de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9167cd2-fc88-46b1-9a26-151955fb606c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 092cf56aea2e246fbb7ef2016a2662a1f67f889b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439519"
---
# <a name="message-store-features"></a>Fonctionnalités de la boutique de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de magasins de messages sont plus complexes que les autres fournisseurs de services MAPI, car ils disposent d’un plus large éventail de fonctionnalités facultatives qu’ils peuvent implémenter. La liste des fonctionnalités requises pour un fournisseur de magasins de messages est relativement courte. Toutefois, un fournisseur de magasin de messages classique prendra en charge un certain nombre de fonctionnalités facultatives, car de nombreuses fonctionnalités facultatives sont très utiles ou requises par la plupart des clients MAPI. Le tableau suivant répertorie les principales fonctionnalités que les fournisseurs de magasins de messages peuvent implémenter et indique si chaque fonctionnalité est requise ou facultative pour tous les fournisseurs de magasins de messages et pour les fournisseurs de magasins de messages par défaut.
  
|**Fonctionnalité**|**All**|**Par défaut**|
|:-----|:-----|:-----|
|Fourniture de l’état avec la table d’état MAPI.  <br/> |Obligatoire  <br/> |Obligatoire  <br/> |
|Mise en œuvre d’objets de dossier.  <br/> |Obligatoire  <br/> |Obligatoire  <br/> |
|Mise en œuvre d’objets de message.  <br/> |Obligatoire  <br/> |Obligatoire  <br/> |
|Fournir des rapports de lecture et nonread.  <br/> |Obligatoire  <br/> |Obligatoire  <br/> |
|Fourniture d’une interface de progression.  <br/> |Obligatoire  <br/> |Obligatoire  <br/> |
|Fourniture d’une interface de configuration.  <br/> |Obligatoire  <br/> |Obligatoire  <br/> |
|Prise en charge des tables de contenu associées pour la prise en charge des formulaires et des affichages.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Envoi de messages avec le fournisseur de la boutique de messages.  <br/> |Facultatif  <br/> |Obligatoire  <br/> |
|Réception de messages avec le fournisseur de la boutique de messages.  <br/> |Facultatif  <br/> |Obligatoire  <br/> |
|Prise en charge des pièces jointes de message.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge du format texte enrichi pour les messages.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Fourniture de notifications.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge des recherches.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge de fournisseurs de transport/magasin de messages étroitement couplés.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge de la non-réutilisation des identificateurs d’entrée.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
   
Bon nombre des fonctionnalités facultatives peuvent être publiées dans MAPI et les applications clientes en paraélisant différents indicateurs dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de l’objet de la boutique de messages. Les fonctionnalités requises ne sont pas associées à des indicateurs. **PR_STORE_SUPPORT_MASK** est nécessaire sur les objets de message, de dossier et de message. 
  
## <a name="see-also"></a>Voir aussi



[Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

