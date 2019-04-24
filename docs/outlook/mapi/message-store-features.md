---
title: Fonctionnalités de banque de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9167cd2-fc88-46b1-9a26-151955fb606c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 092cf56aea2e246fbb7ef2016a2662a1f67f889b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356902"
---
# <a name="message-store-features"></a>Fonctionnalités de banque de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de banque de messages sont plus complexes que d'autres fournisseurs de services MAPI dans ce dernier les fournisseurs de banques de messages disposent d'un large éventail de fonctionnalités facultatives qu'ils peuvent implémenter. La liste des fonctionnalités requises pour un fournisseur de banque de messages est relativement courte. Toutefois, un fournisseur de banque de messages classique prend en charge un certain nombre de fonctionnalités facultatives, car de nombreuses fonctionnalités facultatives sont très utiles ou requises par la plupart des clients MAPI. Le tableau suivant répertorie les principales fonctionnalités que les fournisseurs de banques de messages peuvent implémenter et indique si chaque fonctionnalité est requise ou facultative pour tous les fournisseurs de banques de messages et pour les fournisseurs de banques de messages par défaut.
  
|**Fonctionnalité**|**All**|**Par défaut**|
|:-----|:-----|:-----|
|Fourniture de l'état avec la table d'État MAPI.  <br/> |Obligatoire  <br/> |Obligatoire  <br/> |
|Implémentation des objets de dossier.  <br/> |Obligatoire  <br/> |Obligatoire  <br/> |
|Implémentation d'objets message.  <br/> |Obligatoire  <br/> |Obligatoire  <br/> |
|Fournir des rapports de lecture et nonread.  <br/> |Obligatoire  <br/> |Obligatoire  <br/> |
|Fourniture d'une interface de progression.  <br/> |Obligatoire  <br/> |Obligatoire  <br/> |
|Fourniture d'une interface de configuration.  <br/> |Obligatoire  <br/> |Obligatoire  <br/> |
|Prise en charge des tables de contenu associées pour la prise en charge des formulaires et des vues.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Envoi de messages à l'aide du fournisseur de banque de messages.  <br/> |Facultatif  <br/> |Obligatoire  <br/> |
|Réception de messages avec le fournisseur de banque de messages.  <br/> |Facultatif  <br/> |Obligatoire  <br/> |
|Prise en charge des pièces jointes.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge du format RTF pour les messages.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Fourniture de notifications.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Les recherches de prise en charge.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge de fournisseurs de transport et de banques de messages étroitement couplés.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge de la non-réutilisation des identificateurs d'entrée.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
   
De nombreuses fonctionnalités facultatives peuvent être annoncées dans les applications MAPI et clientes en définissant différents indicateurs dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de l'objet Banque de messages. Les fonctionnalités requises ne sont pas associées à des indicateurs. **PR_STORE_SUPPORT_MASK** est requis sur les objets de banque de messages, de dossier et de message. 
  
## <a name="see-also"></a>Voir aussi



[Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

