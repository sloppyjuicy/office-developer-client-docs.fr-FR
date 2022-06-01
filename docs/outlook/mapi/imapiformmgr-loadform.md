---
title: IMAPIFormMgrLoadForm
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPIFormMgrLoadForm, qui démarre un formulaire pour ouvrir un message existant.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.LoadForm
api_type:
- COM
ms.assetid: 5ca500c3-c737-45a5-b0fc-473b75c1d68d
ms.openlocfilehash: 7c0d324c6cbf7ca58b805f744b8b64d1d6206296
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812186"
---
# <a name="imapiformmgrloadform"></a>IMAPIFormMgr::LoadForm

**S’applique à** : Outlook 2013 | Outlook 2016
  
Démarre un formulaire pour ouvrir un message existant.
  
```cpp
HRESULT LoadForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pmsg,
  LPMAPIVIEWCONTEXT pViewContext,
  REFIID riid,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Handle de la fenêtre parente de l’indicateur de progression qui s’affiche pendant l’ouverture du formulaire. Le paramètre _ulUIParam_ est ignoré, sauf si l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ .

 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la façon dont le formulaire est ouvert. Les indicateurs suivants peuvent être définis :

MAPI_DIALOG
  
> Affiche une interface utilisateur pour fournir l’état ou inviter l’utilisateur à obtenir plus d’informations. Si cet indicateur n’est pas défini, aucune interface utilisateur n’est affichée.

MAPIFORM_EXACTMATCH
  
> Seules les chaînes de classe de message qui correspondent exactement doivent être résolues.

 _lpszMessageClass_
  
> [in] Pointeur vers une chaîne qui nomme la classe de message du message à charger. Si NULL est passé dans le paramètre _lpszMessageClass_ , la classe de message est déterminée à partir du message pointé par le paramètre _pmsg_ .

 _ulMessageStatus_
  
> [in] Masque de bits d’indicateurs définis par le client ou définis par le fournisseur copiés à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message qui fournit des informations sur l’état du message. Le paramètre _ulMessageStatus_ doit être défini si _lpszMessageClass_ n’est pas NULL ; sinon, _ulMessageStatus_ est ignoré.

 _ulMessageFlags_
  
> [in] Pointeur vers un masque de bits d’indicateurs copiés à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message qui indique l’état actuel du message. Le paramètre _ulMessageFlags_ doit être défini si _lpszMessageClass_ n’est pas NULL ; sinon, _ulMessageFlags_ est ignoré.

 _pFolderFocus_
  
> [in] Pointeur vers le dossier qui contient directement le message. Le paramètre _pFolderFocus_ peut être NULL si un tel dossier n’existe pas (par exemple, si le message est incorporé dans un autre message).

 _pMessageSite_
  
> [in] Pointeur vers le site de message du message.

 _pmsg_
  
> [in] Pointeur vers le message.

 _pViewContext_
  
> [in] Pointeur vers le contexte d’affichage du message. Le paramètre _pViewContext_ peut être NULL.

 _Riid_
  
> [in] Identificateur d’interface (IID) de l’interface à utiliser pour l’objet de formulaire retourné. Le paramètre _riid_ ne doit pas être NULL.

 _ppvObj_
  
> [out] Pointeur vers un pointeur vers l’interface retournée.

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.

MAPI_E_NO_INTERFACE
  
> Le formulaire ne prend pas en charge l’interface demandée.

MAPI_E_NOT_FOUND
  
> La classe de message passée dans _lpszMessageClass_ ne correspond à la classe de message pour aucun formulaire de la bibliothèque de formulaires.

## <a name="remarks"></a>Remarques

Les visionneuses de formulaire appellent la méthode **IMAPIFormMgr::LoadForm** pour ouvrir un formulaire pour un message existant. **LoadForm** ouvre l’objet de formulaire, charge le message dans l’objet de formulaire, configure le contexte d’affichage approprié, si nécessaire, et retourne l’interface demandée pour l’objet de formulaire.
  
Le paramètre _pFolderFocus_ pointe vers le dossier qui contient le message. Si le message est incorporé dans un autre message, _pFolderFocus_ doit avoir la valeur NULL.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si NULL est passé dans _lpszMessageClass_, l’implémentation obtient la classe de message, l’état et les indicateurs du message à partir des **propriétés PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** et **PR_MESSAGE_FLAGS** . Si une chaîne de classe de message est fournie dans _lpszMessageClass_, l’implémentation doit utiliser les valeurs dans _ulMessageStatus_ et _ulMessageFlags_.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr::LoadForm** pour charger un formulaire avant de l’afficher. |

## <a name="see-also"></a>Voir aussi

[Propriété canonique PidTagMessageClass](pidtagmessageclass-canonical-property.md)  
[Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)
 [MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
