---
title: IMAPISessionQueryIdentity
description: IMAPISessionQueryIdentity retourne l’identificateur d’entrée de l’objet qui fournit l’identité principale de la session.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.QueryIdentity
api_type:
- COM
ms.assetid: a2cdda90-5457-49a7-b98c-7273ffe5cbbc
ms.openlocfilehash: 60fadd3226c57e96fc0023856d96b2495a09e508
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827932"
---
# <a name="imapisessionqueryidentity"></a>IMAPISession::QueryIdentity

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne l’identificateur d’entrée de l’objet qui fournit l’identité principale de la session.
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Paramètres

 _lpcbEntryID_
  
> [out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée de l’objet qui fournit l’identité primaire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’identité principale a été retournée avec succès.
    
MAPI_W_NO_SERVICE 
  
> L’appel a réussi, mais il n’existe aucune identité principale pour la session. Lorsque cet avertissement est retourné, l’appel doit être traité comme ayant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::QueryIdentity** récupère l’identité principale de la session active et retourne la valeur via le paramètre  _lppEntryID_ . L’identité principale est un objet, généralement un utilisateur de messagerie, qui représente l’utilisateur d’une session.  _lppEntryID_ retourne l’identité principale d’un objet [IMailUser](imailuserimapiprop.md) , qui est également stocké en tant que propriété [PidTagEntryID](pidtagentryid-canonical-property.md) . Vous pouvez utiliser la valeur retournée dans  _lppEntryID_ pour ouvrir un objet **IMailUser à l’aide** [d’IMAPISession::OpenEntry](imapisession-openentry.md).
  
Bien que de nombreux fournisseurs de services dans plusieurs services de messages puissent fournir l’identité principale d’une session, MAPI désigne un fournisseur de services unique. Le fournisseur de services qui fournit l’identité principale définit les éléments suivants :
  
- Indicateur STATUS_PRIMARY_IDENTITY dans la propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- Propriété **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).
    
- Propriété **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).
    
- Propriété **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).
    
Si le fournisseur de services qui fournit l’identité principale appartient à un service de message, les autres fournisseurs de services dans le service de message définissent également les propriétés PR_IDENTITY. Ces propriétés sont publiées dans la table d’état de la session. 
  
Si possible, **QueryIdentity** retourne la valeur de la propriété **PR_IDENTITY_ENTRYID** à partir de la ligne d’état marquée avec STATUS_PRIMARY_IDENTITY. Si la propriété **PR_IDENTITY_ENTRYID** est manquante dans la ligne d’identité principale, **QueryIdentity** retourne un identificateur d’entrée unique créé avec d’autres informations de cette ligne. 
  
Si l’indicateur STATUS_PRIMARY_IDENTITY est manquant dans toutes les colonnes **PR_RESOURCE_FLAG** de la table d’état, **QueryIdentity** retourne le premier identificateur d’entrée qu’il trouve. Lorsqu’il n’existe aucun identificateur d’entrée approprié à retourner, **QueryIdentity** réussit avec l’MAPI_W_NO_SERVICE d’avertissement et pointe  _lppEntryID_ vers un identificateur d’entrée codé en dur. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez appeler la méthode [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) pour affecter à un service de message la tâche de fournir l’identité principale de la session. 
  
Une autre façon de récupérer l’identité principale consiste à rechercher dans la table d’état la ligne avec les colonnes **PR_RESOURCE_FLAGS** définies sur STATUS_PRIMARY_IDENTITY. Pour plus d’informations sur cette autre façon de récupérer des informations d’identité, consultez [La table d’état et les objets d’état](status-table-and-status-objects.md).
  
Lorsque vous avez terminé d’utiliser l’identificateur d’entrée pour l’identité primaire retournée par **QueryIdentity**, libérez sa mémoire en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour plus d’informations sur l’identité en général, consultez [l’identité primaire MAPI](mapi-primary-identity.md). 
  
Pour plus d’informations sur la récupération de l’identité de session MAPI, consultez [Récupération de l’identité principale et de l’identité du fournisseur](retrieving-primary-and-provider-identity.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnQueryIdentity  <br/> |MFCMAPI utilise la méthode **IMAPISession::QueryIdentity** pour ouvrir l’entrée du carnet d’adresses pour l’identité principale de la session. |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Identité principale MAPI](mapi-primary-identity.md)
  
[Récupération de l’identité principale et de l’identité du fournisseur](retrieving-primary-and-provider-identity.md)
  
[Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)
  
[Table d’état et objets d’état](status-table-and-status-objects.md)

