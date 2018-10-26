---
title: Fonctionnalités de banque de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9167cd2-fc88-46b1-9a26-151955fb606c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7e99d9d2e1289ed98ba659e97b05c8ea6d891a74
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581810"
---
# <a name="message-store-features"></a>Fonctionnalités de banque de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournisseurs de banque de messages sont plus complexes que les autres fournisseurs de services MAPI : fournisseurs de banque de message ont un large éventail de fonctionnalités facultatives, qu'ils peuvent mettre en œuvre. La liste des fonctionnalités requises pour un fournisseur de banque de messages est relativement courte. Toutefois, un fournisseur de magasin de message par défaut prendront en charge un nombre de fonctionnalités facultatives, étant donné que de nombreuses fonctionnalités facultatives sont très utiles ou requises par la plupart des clients MAPI. Le tableau suivant répertorie les principales fonctionnalités que les fournisseurs de magasins de message peuvent mettre en œuvre et si chaque fonctionnalité est obligatoire ou facultatif pour tous les messages de stocker les fournisseurs et de message par défaut pour les fournisseurs de magasin de.
  
|**Fonctionnalité**|**All**|**Default**|
|:-----|:-----|:-----|
|Fourniture d’état avec la table d’état MAPI.  <br/> |Required  <br/> |Required  <br/> |
|Implémentation d’objets de dossier.  <br/> |Required  <br/> |Required  <br/> |
|Implémentation d’objets de message.  <br/> |Required  <br/> |Required  <br/> |
|Fournir des rapports de lecture et nonread.  <br/> |Required  <br/> |Required  <br/> |
|Fourniture d’une interface de progression.  <br/> |Required  <br/> |Required  <br/> |
|Fourniture d’une interface de configuration.  <br/> |Required  <br/> |Required  <br/> |
|Prise en charge des tableaux de contenu associé pour la prise en charge des formulaires et des vues.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Fournisseur de magasin d’envoi de messages avec le message.  <br/> |Facultatif  <br/> |Obligatoire  <br/> |
|Réception de messages avec le fournisseur de banque de messages.  <br/> |Facultatif  <br/> |Obligatoire  <br/> |
|Prise en charge des pièces jointes des messages.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge le Format RTF pour les messages.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Fournir des notifications.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge des recherches.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge étroitement couplés fournisseurs de banque/transport de message.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
|Prise en charge non réutilisation d’identificateurs d’entrée.  <br/> |Facultatif  <br/> |Facultatif  <br/> |
   
De nombreuses fonctionnalités facultatives peuvent être publiés dans MAPI et stockent les applications clientes en définissant des indicateurs différents dans le message propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de l’objet. Les fonctionnalités requises n’ont pas d’indicateurs qui leur sont associées. **PR_STORE_SUPPORT_MASK** est requis sur la banque de messages, de dossiers et les objets de message. 
  
## <a name="see-also"></a>Voir aussi



[Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

