---
title: L’implémentation d’une Table unique du fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 99146f93dcf634be6766f5c6fcc0d1c610b84d4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784169"
---
# <a name="implementing-a-provider-one-off-table"></a>L’implémentation d’une Table unique du fournisseur

  
  
**S’applique à**: Outlook 
  
MAPI appelle la méthode [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) de votre fournisseur lorsque l’utilisateur d’une application cliente ajoute un destinataire à un message sortant. En règle générale, les types d’adresses demandés sont spécifiques à votre système de messagerie. Si votre fournisseur prend en charge la création de destinataires, elle doit fournir une table unique qui expose des modèles pour chaque type d’adresse du destinataire pris en charge. Si votre fournisseur ne gère pas la création de destinataires, renvoyer MAPI_E_NO_SUPPORT à partir de l’appel **GetOneOffTable** . 
  
MAPI généralement conserve table uniques de votre fournisseur ouvert pour la durée de vie de la session, libérer uniquement lorsqu’un client appelle soit du sous-système ou méthode de [IMAPIStatus::ValidateState](imapistatus-validatestate.md) du carnet d’adresses. MAPI inscrit pour les notifications sur ce tableau afin que si les modèles sont ajoutées ou supprimées, ces modifications peuvent être reflétées à l’utilisateur. 
  
 **Pour mettre en œuvre IABLogon::GetOneOffTable**
  
1. Vérifiez la valeur du paramètre flags, _ulFlags_. Si l’indicateur MAPI_UNICODE est défini et que votre fournisseur ne prend pas en charge Unicode, échouer et retourner MAPI_E_BAD_CHARWIDTH. 
    
2. Vérifiez si uniques table votre fournisseur a déjà été créée. Étant donné que les tables uniques sont généralement statiques, votre fournisseur n’a jamais transitent par le processus de création de plusieurs fois. Si une table existe déjà, retourne un pointeur à celui-ci. 
    
3. Si une table unique n’existe pas, appelez **Create table** pour en créer une. 
    
4. Définissez les propriétés suivantes pour les colonnes dans les lignes de la table :
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) sur le nom du type de destinataire que le modèle peut créer. 
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à l’identificateur d’entrée pour le modèle unique.
    
  - **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) pour indiquer le niveau de hiérarchie dans l’affichage tableau uniques.
    
  - **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) la valeur True pour indiquer si la ligne représente un modèle et la valeur FALSE.
    
  - **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) pour le type d’adresse créé par le modèle.
    
  - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) DT_MAILUSER ou une autre valeur qui indique le type d’affichage pour le modèle.
    
  - **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) une valeur binaire unique. 
    
5. Appelez [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) pour modifier la table directement. 
    
6. Appelez [ITableData::HrGetView](itabledata-hrgetview.md) pour créer une implémentation d’interface **IMAPITable** pour revenir à l’appelant. 
    

