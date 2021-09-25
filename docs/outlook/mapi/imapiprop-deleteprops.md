---
title: IMAPIPropDeleteProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.DeleteProps
api_type:
- COM
ms.assetid: 5cc642de-21f0-4826-bf21-aac4bcfc1328
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 036ec32924c8bbb0a305b46558180bfe25e02777
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564133"
---
# <a name="imapipropdeleteprops"></a>IMAPIProp::DeleteProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime une ou plusieurs propriétés d’un objet. 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Paramètres

 _lpPropTagArray_
  
> [in] Pointeur vers un tableau de balises de propriétés qui indiquent les propriétés à supprimer. Le membre **cValues** de la structure [SPropTagArray](sproptagarray.md) pointée par  _lpPropTagArray_ ne doit pas être zéro et le paramètre  _lpPropTagArray_ lui-même ne doit pas être NULL. 
    
 _lppProblems_
  
> [in, out] Lors de l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; sinon, NULL, qui indique qu’il n’est pas nécessaire d’obtenir des informations d’erreur. Si  _lppProblems est_ un pointeur valide sur l’entrée, **DeleteProps** renvoie des informations détaillées sur les erreurs de suppression d’une ou de plusieurs propriétés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les propriétés ont été supprimées avec succès.
    
MAPI_E_NO_ACCESS 
  
> L’appelant ne dispose pas des autorisations suffisantes pour supprimer des propriétés.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIProp::D eleteProps** supprime une ou plusieurs propriétés de l’objet actuel. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous n’avez pas besoin d’autoriser la suppression des propriétés de tous les objets. Si l’objet n’est pas modifiable, renvoyez MAPI_E_NO_ACCESS la **méthode DeleteProps.** 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Il n’est pas nécessaire de définir le type de propriété pour chaque balise de propriété dans le tableau de balises de propriétés pointant vers le _paramètre lpPropTagArray._ Les types de propriétés sont ignorés ; seuls les identificateurs de propriété sont utilisés. 
  
Notez que certains objets n’autorisent pas la modification et que ces objets MAPI_E_NO_ACCESS à partir de **la méthode DeleteProps.** D’autres objets permettent la suppression de certaines propriétés, mais pas d’autres. En cas de problème de suppression de certaines propriétés uniquement, **DeleteProps** renvoie S_OK. Si vous avez passé un pointeur valide dans le paramètre  _lppProblems,_ **DeleteProps** le définira sur une structure **SPropProblemArray** qui contient des informations détaillées sur les problèmes liés à chaque propriété. Par exemple, si vous êtes en cours de suppression de toutes les propriétés d’un message et qu’il existe un problème avec une ou plusieurs de ses pièces jointes, la structure **SPropProblemArray** contient une entrée pour la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
La structure pointée par  _lppProblems n’est_ valide que **si DeleteProps** renvoie S_OK. Si **DeleteProps renvoie** une erreur, n’essayez pas d’utiliser la structure **SPropProblemArray.** Appelez plutôt la méthode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) de l’objet pour obtenir plus d’informations sur l’erreur. 
  
Libérez la structure **SPropProblemArray** renvoyée en appelant la [fonction MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |DeleteProperty  <br/> |MFCMAPI utilise **la méthode IMAPIProp::D eleteProps** pour supprimer une propriété d’un objet.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

