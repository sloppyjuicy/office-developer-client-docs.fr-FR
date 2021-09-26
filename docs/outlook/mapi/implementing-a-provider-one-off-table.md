---
title: Mise en œuvre d’une table One-Off fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 060f69c28484b8fe3a805af22ebe631c746425de
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620785"
---
# <a name="implementing-a-provider-one-off-table"></a>Mise en œuvre d’une table One-Off fournisseur

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI appelle la méthode [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) de votre fournisseur lorsque l’utilisateur d’une application cliente ajoute un destinataire à un message sortant. En règle générale, les types d’adresses demandés sont propres à votre système de messagerie. Si votre fournisseur prend en charge la création de destinataires, il doit fournir un tableau unique qui expose des modèles pour chaque type d’adresse de destinataire prise en charge. Si votre fournisseur ne prend pas en charge la création de destinataires, MAPI_E_NO_SUPPORT à partir de **l’appel GetOneOffTable.** 
  
MAPI conserve généralement la table unique de votre fournisseur ouverte pendant toute la durée de vie de la session, en la libérant uniquement lorsqu’un client appelle la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) du sous-système ou du carnet d’adresses. MAPI s’inscrit pour les notifications dans ce tableau afin que si des modèles sont ajoutés ou supprimés, ces modifications peuvent être reflétées pour l’utilisateur. 
  
 **Pour implémenter IABLogon::GetOneOffTable**
  
1. Vérifiez la valeur du paramètre d’indicateurs,  _ulFlags_. Si l’MAPI_UNICODE est définie et que votre fournisseur ne prend pas en charge Unicode, échouez et renvoyez MAPI_E_BAD_CHARWIDTH. 
    
2. Vérifiez si la table one-off de votre fournisseur a déjà été créée. Étant donné que les tables unique sont généralement statiques, votre fournisseur n’a jamais à passer par le processus de création plusieurs fois. Si un tableau existe déjà, renvoyer un pointeur vers ce tableau. 
    
3. Si une table non existante n’existe pas encore, appelez **CreateTable** pour en créer une. 
    
4. Définissez les propriétés suivantes pour les colonnes dans les lignes de votre tableau :
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) au nom du type de destinataire que le modèle peut créer. 
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à l’identificateur d’entrée pour le modèle unique.
    
  - **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) pour indiquer le niveau de hiérarchie dans l’affichage du tableau.
    
  - **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) à TRUE pour indiquer si la ligne représente un modèle et FALSE dans le cas contraire.
    
  - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) au type d’adresse créé par le modèle.
    
  - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) pour DT_MAILUSER ou une autre valeur qui indique le type d’affichage pour le modèle.
    
  - **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) à une valeur binaire unique. 
    
5. Appelez [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) pour modifier directement la table. 
    
6. Appelez [ITableData::HrGetView](itabledata-hrgetview.md) pour créer une implémentation d’interface **IMAPITable** pour revenir à l’appelant. 
    

