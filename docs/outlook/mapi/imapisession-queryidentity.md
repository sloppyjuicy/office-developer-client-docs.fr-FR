---
title: IMAPISessionQueryIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.QueryIdentity
api_type:
- COM
ms.assetid: a2cdda90-5457-49a7-b98c-7273ffe5cbbc
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 396320c6b39553da09aa1f45d0c755f40a939382
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335692"
---
# <a name="imapisessionqueryidentity"></a>IMAPISession::QueryIdentity

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie l'identificateur d'entrée de l'objet qui fournit l'identité principale pour la session.
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Paramètres

 _lpcbEntryID_
  
> remarquer Pointeur vers le nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lppEntryID_ . 
    
 _lppEntryID_
  
> remarquer Pointeur vers un pointeur vers l'identificateur d'entrée de l'objet qui fournit l'identité principale.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'identité principale a été correctement renvoyée.
    
MAPI_W_NO_SERVICE 
  
> L'appel a réussi, mais il n'existe pas d'identité principale pour la session. Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession:: QueryIdentity** extrait l'identité principale de la session en cours et renvoie la valeur via le paramètre _lppEntryID_ . L'identité principale est un objet, généralement un utilisateur de messagerie, qui représente l'utilisateur d'une session.  _lppEntryID_ renvoie l'identité principale d'un objet [IMailUser](imailuserimapiprop.md) , qui est également stockée en tant que propriété [PidTagEntryID](pidtagentryid-canonical-property.md) . Vous pouvez utiliser la valeur renvoyée dans _lppEntryID_ pour ouvrir un objet **IMailUser** à l'aide de [IMAPISession:: OpenEntry](imapisession-openentry.md).
  
Bien que de nombreux fournisseurs de services dans plusieurs services de messagerie puissent fournir l'identité principale pour une session, MAPI désigne un seul fournisseur de services. Le fournisseur de services qui fournit l'identité principale définit les éléments suivants:
  
- L'indicateur STATUS_PRIMARY_IDENTITY dans la propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- Propriété **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).
    
- Propriété **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).
    
- Propriété **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).
    
Si le fournisseur de services qui fournit l'identité principale appartient à un service de messagerie, les autres fournisseurs de services du service de messagerie définissent également les propriétés PR_IDENTITY. Ces propriétés sont publiées dans la table d'état de la session. 
  
Dans la mesure du possible, **QueryIdentity** renvoie la valeur de la propriété **PR_IDENTITY_ENTRYID** à partir de la ligne d'État marquée avec STATUS_PRIMARY_IDENTITY. Si la propriété **PR_IDENTITY_ENTRYID** est absente de la ligne d'identité principale, **QueryIdentity** renvoie un identificateur d'entrée unique créé avec d'autres informations à partir de cette ligne. 
  
Si l'indicateur STATUS_PRIMARY_IDENTITY est absent de toutes les colonnes **PR_RESOURCE_FLAG** de la table d'État, **QueryIdentity** renvoie le premier identificateur d'entrée qu'il trouve. Lorsqu'il n'existe pas d'identificateur d'entrée approprié à renvoyer, **QueryIdentity** réussit avec l'avertissement MAPI_W_NO_SERVICE et pointe _lppEntryID_ vers un identificateur d'entrée codé en dur. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez appeler la méthode [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) pour affecter un service de message à la tâche de fourniture de l'identité principale de la session. 
  
Pour récupérer l'identité principale, une autre méthode consiste à rechercher la ligne à l'aide des colonnes **PR_RESOURCE_FLAGS** définies sur STATUS_PRIMARY_IDENTITY dans la table d'État. Pour plus d'informations sur cette autre façon de récupérer des informations d'identité, voir [table d'État et objets d'État](status-table-and-status-objects.md).
  
Lorsque vous avez terminé d'utiliser l'identificateur d'entrée pour l'identité principale renvoyée par **QueryIdentity**, libérez sa mémoire en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour plus d'informations sur l'identité en général, consultez la rubrique [MAPI Primary Identity](mapi-primary-identity.md). 
  
Pour plus d'informations sur la récupération de l'identité de session MAPI, consultez la rubrique [extraction des identités principales et des fournisseurs](retrieving-primary-and-provider-identity.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnQueryIdentity  <br/> |MFCMAPI utilise la méthode **IMAPISession:: QueryIdentity** pour ouvrir l'entrée de carnet d'adresses pour l'identité principale de la session.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Identité principale MAPI](mapi-primary-identity.md)
  
[Récupération de l'identité principale et de l'identité du fournisseur](retrieving-primary-and-provider-identity.md)
  
[Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)
  
[Table d'État et objets d'État](status-table-and-status-objects.md)

