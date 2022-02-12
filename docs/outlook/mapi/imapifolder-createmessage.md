---
title: IMAPIFolderCreateMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.CreateMessage
api_type:
- COM
ms.assetid: e0222afa-c148-4735-a603-cac7be6c91f9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dcc6fa748c4e539afa4adb67344966093d11b9ca
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773611"
---
# <a name="imapifoldercreatemessage"></a>IMAPIFolder::CreateMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un message.
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a>Paramètres

 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au nouveau message. Les identificateurs d’interface valides incluent IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer et IID_IMAPIFolder. Si la valeur NULL est passé, le fournisseur de magasin de messages retourne l’interface de message standard [, IMessage : IMAPIProp](imessageimapiprop.md). 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le message est créé. Les indicateurs suivants peuvent être définies :
    
ITEMPROC_FORCE
  
> Indique au magasin de dossiers personnels (PST) que le message est éligible pour le traitement des règles avant que la boutique n’avertisse le client d’écoute de l’arrivée du nouveau message. Le traitement des règles s’applique uniquement aux nouveaux messages créés sur un serveur qui n’est pas un serveur Microsoft Exchange Server, car Exchange Server les règles pour les messages sur le serveur. Par conséquent, le fournisseur ou le client qui crée le message doit passer cet indicateur en combinaison avec l’enregistrement d’un message avec [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) à l’aide de NON_EMS_XP_SAVE, ce qui indique que le serveur n’est pas un Exchange Server. 
    
MAPI_ASSOCIATED 
  
> Le message à créer doit être inclus dans la table des matières associée au lieu de la table des matières standard. Les messages associés sont masqués lors de l’interaction utilisateur.
    
MAPI_DEFERRED_ERRORS 
  
> **CreateMessage est autorisé** à réussir même si l’opération de création n’est pas entièrement terminée. Cela implique que le nouveau message ne soit peut-être pas immédiatement disponible pour l’appelant. 
    
 _lppMessage_
  
> [out] Pointeur vers un pointeur vers le message nouvellement créé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le message a été créé avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIFolder::CreateMessage** crée un message avec un contenu générique ou associé et affecte un identificateur d’entrée. L’identificateur d’entrée se compose d’une partie qui représente le fournisseur de la boutique de messages et d’une partie qui représente le message individuel. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez choisir de définir toutes les **propriétés de message requises dans CreateMessage** ou dans la méthode [IMAPIProp::SaveChanges du](imapiprop-savechanges.md) message. Vous n’avez pas besoin de rendre ces propriétés disponibles tant qu’un sauvegarde réussi n’a pas eu lieu. 
  
Pour plus d’informations sur l’emploi des informations associées, voir [Folder-Associated Information Tables](folder-associated-information-tables.md) and [Contents Tables](contents-tables.md). 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Certains fournisseurs de magasins de messages permettent que l’identificateur d’entrée du nouveau message soit disponible immédiatement après le retour de **CreateMessage** . d’autres fournisseurs de magasins de messages retardent sa disponibilité jusqu’à ce que le message soit enregistré. Étant donné que tous les fournisseurs de magasins de messages ne génèrent pas d’identificateur d’entrée pour un nouveau message tant que vous n’avez pas appelé la méthode **IMAPIProp::SaveChanges** du message, il se peut que vous ne soyez pas en mesure d’accéder à l’identificateur d’entrée lorsque **CreateMessage** est de retour. En outre, le nouveau message peut ne pas être inclus dans la table des matières du dossier tant que l’opération d’enregistrer n’a pas eu lieu. 
  
Attendez-vous à ce que l’identificateur d’entrée affecté au nouveau message soit unique non seulement dans la boutique de messages actuelle, mais probablement dans toutes les magasins de messages ouverts en même temps. Une exception à cette règle se produit lorsque plusieurs entrées d’une magasin de messages apparaissent dans le profil. Cela entraîne l’ouverture multiple de la magasin de messages et la duplication des identificateurs d’entrée. 
  
Pour créer un message sortant, appelez la méthode **IMAPIFolder::CreateMessage** du dossier Outbox. 
  
Si vous supprimez un dossier qui contient un nouveau message avant que le message ne soit enregistré, les résultats ne sont pas indéfinis.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolder::OnNewMessage  <br/> |MFCMAPI utilise la **méthode IMAPIFolder::CreateMessage** pour créer et enregistrer un nouveau message. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

