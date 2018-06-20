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
ms.openlocfilehash: c8f05707d63f922c9ce22e6e520c6c57e686f884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783951"
---
# <a name="imapisessionqueryidentity"></a>IMAPISession::QueryIdentity

  
  
**S’applique à**: Outlook 
  
Renvoie l’identificateur d’entrée de l’objet qui fournit l’identité du principale pour la session.
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Paramètres

 _lpcbEntryID_
  
> [out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée de l’objet qui fournit l’identité du principale.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’identité du principale a été renvoyée avec succès.
    
MAPI_W_NO_SERVICE 
  
> L’appel a réussi, mais il n’existe aucune identité principale pour la session. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::QueryIdentity** récupère l’identité du principale pour la session en cours et renvoie la valeur via le paramètre _lppEntryID_ . L’identité du principale est un objet, généralement un utilisateur de messagerie, qui représente l’utilisateur d’une session.  _lppEntryID_ renvoie l’identité du principale pour un objet [IMailUser](imailuserimapiprop.md) , qui est également stockée dans la propriété [PidTagEntryID](pidtagentryid-canonical-property.md) . Vous pouvez utiliser la valeur renvoyée dans _lppEntryID_ pour ouvrir un objet **IMailUser** à l’aide de [IMAPISession::OpenEntry](imapisession-openentry.md).
  
Bien que plusieurs fournisseurs de services de plusieurs services de messagerie peuvent fournir l’identité du principale d’une session, MAPI désigne un fournisseur de service unique. Le fournisseur de services qui fournit l’identité principale définit les éléments suivants :
  
- L’indicateur STATUS_PRIMARY_IDENTITY dans la propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- La propriété **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).
    
- La propriété **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).
    
- La propriété **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).
    
Si le fournisseur de services qui fournit l’identité du principale appartient à un service de message, les fournisseurs de services dans le service message également définir les propriétés PR_IDENTITY. Ces propriétés sont publiées dans la table d’état de la session. 
  
Si possible, **QueryIdentity** renvoie la valeur de la propriété **PR_IDENTITY_ENTRYID** à partir de la ligne d’état marquée avec STATUS_PRIMARY_IDENTITY. Si la propriété **PR_IDENTITY_ENTRYID** est manquante dans la ligne d’identité principale, **QueryIdentity** renvoie un identificateur d’entrée unique intégré avec d’autres informations de cette ligne. 
  
Si l’indicateur STATUS_PRIMARY_IDENTITY est manquante à partir de toutes les colonnes dans la table d’état **PR_RESOURCE_FLAG** , **QueryIdentity** renvoie l’identificateur d’entrée première qu’il trouve. Lorsqu’il n’existe aucun identificateur d’entrée appropriée à renvoyer, **QueryIdentity** réussit et l’avertissement MAPI_W_NO_SERVICE et pointe _lppEntryID_ vers un identificateur d’entrée codées en dur. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez appeler la méthode [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) pour assigner un service de message de la tâche de fournir l’identité principale de la session. 
  
Une autre manière de récupérer l’identité principale est en recherchant la table d’état de la ligne avec les colonnes **PR_RESOURCE_FLAGS** définis sur STATUS_PRIMARY_IDENTITY. Pour plus d’informations sur cet autre façon de récupérer les informations d’identité, consultez la [Table d’état et les objets d’état](status-table-and-status-objects.md).
  
Lorsque vous avez terminé à l’aide de l’identificateur d’entrée pour l’identité du principale renvoyée par **QueryIdentity**, libérer la mémoire en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour plus d’informations sur l’identité en général, voir [Identité principale MAPI](mapi-primary-identity.md). 
  
Pour plus d’informations sur la récupération d’identité de session MAPI, voir [récupération principal et le fournisseur d’identité](retrieving-primary-and-provider-identity.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnQueryIdentity  <br/> |MFCMAPI utilise la méthode **IMAPISession::QueryIdentity** pour ouvrir l’entrée du carnet d’adresses pour l’identité du principale de la session.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Identité principale MAPI](mapi-primary-identity.md)
  
[Extraction de principal et identité du fournisseur](retrieving-primary-and-provider-identity.md)
  
[Utilisation de Macros pour la gestion des erreurs](using-macros-for-error-handling.md)
  
[Table d’état et les objets d’état](status-table-and-status-objects.md)

