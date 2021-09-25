---
title: IMAPISessionQueryIdentity
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4d1bbe972f7b5a3223cc53a45aaefb08c85c8eb2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584415"
---
# <a name="imapisessionqueryidentity"></a>IMAPISession::QueryIdentity

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie l’identificateur d’entrée de l’objet qui fournit l’identité principale de la session.
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Paramètres

 _lpcbEntryID_
  
> [out] Pointeur vers le nombre d’byte dans l’identificateur d’entrée pointé par _le paramètre lppEntryID._ 
    
 _lppEntryID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée de l’objet qui fournit l’identité principale.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’identité principale a été renvoyée avec succès.
    
MAPI_W_NO_SERVICE 
  
> L’appel a réussi, mais il n’existe pas d’identité principale pour la session. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED.** Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISession::QueryIdentity** récupère l’identité principale de la session en cours et renvoie la valeur via le paramètre _lppEntryID._ L’identité principale est un objet, généralement un utilisateur de messagerie, qui représente l’utilisateur d’une session.  _lppEntryID renvoie_ l’identité principale d’un objet [IMailUser,](imailuserimapiprop.md) qui est également stocké en tant que [propriété PidTagEntryID.](pidtagentryid-canonical-property.md) Vous pouvez utiliser la valeur renvoyée dans _lppEntryID_ pour ouvrir un objet **IMailUser** à l’aide d’IMAPISession::OpenEntry . [](imapisession-openentry.md)
  
Bien que de nombreux fournisseurs de services dans plusieurs services de messagerie peuvent fournir l’identité principale d’une session, MAPI désigne un fournisseur de services unique. Le fournisseur de services qui fournit l’identité principale définit les éléments suivants :
  
- L STATUS_PRIMARY_IDENTITY dans la **propriété PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- Propriété **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).
    
- Propriété **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).
    
- Propriété **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).
    
Si le fournisseur de services qui fournit l’identité principale appartient à un service de messagerie, les autres fournisseurs de services du service de messagerie définissent également les PR_IDENTITY de messagerie. Ces propriétés sont publiées dans la table d’état de la session. 
  
Si possible, **QueryIdentity** renvoie la valeur de la **propriété PR_IDENTITY_ENTRYID** à partir de la ligne d’état marquée avec STATUS_PRIMARY_IDENTITY. Si la **propriété PR_IDENTITY_ENTRYID** est manquante dans la ligne d’identité principale, **QueryIdentity** renvoie un identificateur d’entrée unique créé avec d’autres informations de cette ligne. 
  
Si l’STATUS_PRIMARY_IDENTITY est absent de toutes les colonnes **PR_RESOURCE_FLAG** dans la table d’état, **QueryIdentity** renvoie le premier identificateur d’entrée trouvé. Lorsqu’il n’existe pas d’identificateur d’entrée approprié à renvoyer, **QueryIdentity** réussit avec l’avertissement MAPI_W_NO_SERVICE et pointe  _lppEntryID_ vers un identificateur d’entrée codé en dur. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez appeler la méthode [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) pour affecter à un service de message la tâche de fourniture de l’identité principale de la session. 
  
Une autre façon de récupérer l’identité principale consiste à rechercher dans le tableau d’état la ligne dont les colonnes **PR_RESOURCE_FLAGS** définies sur STATUS_PRIMARY_IDENTITY. Pour plus d’informations sur cette autre façon de récupérer des informations d’identité, voir [Tableau d’état et Objets d’état.](status-table-and-status-objects.md)
  
Lorsque vous avez terminé d’utiliser l’identificateur d’entrée pour l’identité principale renvoyée par **QueryIdentity**, libérez sa mémoire en appelant la [fonction MAPIFreeBuffer.](mapifreebuffer.md) 
  
Pour plus d’informations sur l’identité en général, voir [MAPI Primary Identity](mapi-primary-identity.md). 
  
Pour plus d’informations sur la récupération de l’identité de session MAPI, voir Récupération de l’identité principale [et de l’identité du fournisseur.](retrieving-primary-and-provider-identity.md) 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnQueryIdentity  <br/> |MFCMAPI utilise la méthode **IMAPISession::QueryIdentity** pour ouvrir l’entrée du carnet d’adresses pour l’identité principale de la session.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[MAPI Primary Identity](mapi-primary-identity.md)
  
[Récupération de l’identité principale et du fournisseur](retrieving-primary-and-provider-identity.md)
  
[Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)
  
[Tableau d’état et objets d’état](status-table-and-status-objects.md)

