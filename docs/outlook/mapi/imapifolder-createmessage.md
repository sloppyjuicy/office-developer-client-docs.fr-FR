---
title: IMAPIFolderCreateMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateMessage
api_type:
- COM
ms.assetid: e0222afa-c148-4735-a603-cac7be6c91f9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8d7e6dfbf9e6a751845adb2319b66462bcde651f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783718"
---
# <a name="imapifoldercreatemessage"></a>IMAPIFolder::CreateMessage

  
  
**S’applique à**: Outlook 
  
Crée un nouveau message.
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a>Paramètres

 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au nouveau message. Identificateurs d’interface valides incluent IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer et IID_IMAPIFolder. Passage de NULL entraîne le fournisseur de banque de messages renvoyer l’interface de message standard, [IMessage : IMAPIProp](imessageimapiprop.md). 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le message est créé. Les indicateurs suivants peuvent être définis :
    
ITEMPROC_FORCE
  
> Indique pour la banque de dossiers personnels (PST) que le message est éligible pour les règles de traitement avant que le magasin notifie n’importe quel client d’écoute de l’arrivée du nouveau message. Traitement uniquement des règles s’applique aux nouveaux messages sont créés sur un serveur qui n’est pas un serveur Microsoft Exchange, car Exchange Server traite les règles pour les messages sur le serveur. Par conséquent, le fournisseur ou le client qui crée le message doit passer cet indicateur en combinaison avec l’enregistrement d’un message avec [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) à l’aide de NON_EMS_XP_SAVE, ce qui indique que le serveur n’est pas un serveur Exchange. 
    
MAPI_ASSOCIATED 
  
> Le message doit être créé doit être inclus dans le tableau contenu associé au lieu de la table des matières standard. Messages associés sont masqués intervention de l’utilisateur.
    
MAPI_DEFERRED_ERRORS 
  
> **CreateMessage** est autorisé à fonctionne même si l’opération de création n’est pas entièrement terminée. Cela implique que le nouveau message peuvent ne pas être immédiatement disponible pour l’appelant. 
    
 _lppMessage_
  
> [out] Pointeur vers un pointeur vers le message nouvellement créé.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le message a été créé avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::CreateMessage** crée un nouveau message avec du contenu générique ou associé et affecte un identificateur d’entrée. L’identificateur d’entrée se compose d’une partie qui représente le fournisseur de banque de messages et un composant qui représente le message individuel. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Vous pouvez choisir s’il faut définir toutes les propriétés de message requis dans **CreateMessage** ou dans la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message. Il est inutile de rendre ces propriétés disponible jusqu'à ce qu’une sauvegarde réussie a eu lieu. 
  
Pour plus d’informations sur l’utilisation des informations associées, voir [Folder-Associated informations Tables](folder-associated-information-tables.md) et [Contenu](contents-tables.md). 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Certains fournisseurs de banque de message permettent l’identificateur d’entrée du message immédiatement après **CreateMessage** renvoie ; autres fournisseurs de banque de message délai sa disponibilité jusqu'à ce que le message est enregistré. Étant donné que tous les fournisseurs de banque de messages génèrent un identificateur d’entrée d’un nouveau message jusqu'à ce que vous avez appelé la méthode **IMAPIProp::SaveChanges** du message, vous ne pourrez pas accéder **CreateMessage** renvoie l’identificateur d’entrée. En outre, le nouveau message ne peut pas être inclus dans la table des matières du dossier jusqu'à ce que l’enregistrement se produit. 
  
Attendez l’identificateur d’entrée affecté vers le nouveau message à être uniques non seulement dans la banque de messages actuel, mais probablement dans toutes les banques de messages qui sont ouverts en même temps. Une exception à cette règle se produit lorsque plusieurs entrées pour une banque de messages s’affichent dans le profil. Ainsi, la banque de messages à ouvrir plusieurs fois et les identificateurs d’entrée à dupliquer. 
  
Pour créer un message sortant, appelez la méthode de **IMAPIFolder::CreateMessage** du dossier boîte d’envoi. 
  
Si vous supprimez un dossier qui contient un nouveau message avant du message est enregistré, les résultats ne sont pas définis.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolder::OnNewMessage  <br/> |MFCMAPI utilise la méthode **IMAPIFolder::CreateMessage** pour créer et enregistrer un nouveau message.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

