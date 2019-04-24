---
title: Implémentation d'une table ponctuelle de fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 023686702b76b5b29acf4304fcfdb3377e8cfcff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332864"
---
# <a name="implementing-a-provider-one-off-table"></a>Implémentation d'une table ponctuelle de fournisseur

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI appelle la méthode [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) de votre fournisseur lorsque l'utilisateur d'une application cliente ajoute un destinataire à un message sortant. En règle générale, les types d'adresses demandées sont uniques à votre système de messagerie. Si votre fournisseur prend en charge la création de destinataires, il doit fournir une table ponctuelle qui expose les modèles pour chaque type d'adresse de destinataire prise en charge. Si votre fournisseur ne prend pas en charge la création de destinataires, retournez MAPI_E_NO_SUPPORT à partir de l'appel **GetOneOffTable** . 
  
MAPI conserve généralement la table ponctuelle de votre fournisseur pendant la durée de vie de la session, uniquement lorsqu'un client appelle la méthode [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) du sous-système ou du carnet d'adresses. MAPI s'inscrit pour les notifications sur cette table de sorte que si des modèles sont ajoutés ou supprimés, ces modifications peuvent être répercutées sur l'utilisateur. 
  
 **Pour implémenter IABLogon:: GetOneOffTable**
  
1. Vérifiez la valeur du paramètre flags, _ulFlags_. Si l'indicateur MAPI_UNICODE est défini et que votre fournisseur ne prend pas en charge Unicode, Fail et Return MAPI_E_BAD_CHARWIDTH. 
    
2. Vérifiez si la table ponctuelle de votre fournisseur a déjà été créée. Étant donné que les tables ponctuelles sont généralement statiques, votre fournisseur n'a jamais à passer par le processus de création plus d'une fois. S'il existe déjà une table, renvoyez un pointeur vers celle-ci. 
    
3. Si une table ponctuelle n'existe pas encore, appelez **CreateTable** pour en créer une. 
    
4. Définissez les propriétés suivantes pour les colonnes de vos lignes de tableau:
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) pour le nom du type de destinataire que le modèle peut créer. 
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à l'identificateur d'entrée pour le modèle isolé.
    
  - **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) pour indiquer le niveau de hiérarchie dans l'affichage de la table ponctuelle.
    
  - **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) à true pour indiquer si la ligne représente un modèle et false dans le cas contraire.
    
  - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) au type d'adresse créé par le modèle.
    
  - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) à DT_MAILUSER ou une autre valeur qui indique le type d'affichage pour le modèle.
    
  - **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) à une valeur binaire unique. 
    
5. Appelez [ITableData:: HrModifyRow](itabledata-hrmodifyrow.md) pour modifier directement la table. 
    
6. Appelez [ITableData:: HrGetView](itabledata-hrgetview.md) pour créer une implémentation d'interface **IMAPITable** pour retourner à l'appelant. 
    

