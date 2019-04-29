---
title: IMAPIPropDeleteProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.DeleteProps
api_type:
- COM
ms.assetid: 5cc642de-21f0-4826-bf21-aac4bcfc1328
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5bfef87baa2dffa4605f9a7afa3833024f514430
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409236"
---
# <a name="imapipropdeleteprops"></a>IMAPIProp::DeleteProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime une ou plusieurs propriétés d'un objet. 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Paramètres

 _lpPropTagArray_
  
> dans Pointeur vers un tableau de balises de propriété indiquant les propriétés à supprimer. Le membre **cValues** de la structure [SPropTagArray](sproptagarray.md) vers laquelle pointe _lpPropTagArray_ ne doit pas être égal à zéro et le paramètre _lpPropTagArray_ lui-même ne doit pas être null. 
    
 _lppProblems_
  
> [in, out] Lors de l'entrée, pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; Sinon, NULL, ce qui indique qu'il n'est pas nécessaire d'obtenir des informations sur l'erreur. Si _lppProblems_ est un pointeur valide sur l'entrée, **DeleteProps** renvoie des informations détaillées sur les erreurs lors de la suppression d'une ou de plusieurs propriétés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les propriétés ont été supprimées avec succès.
    
MAPI_E_NO_ACCESS 
  
> L'appelant ne dispose pas des autorisations suffisantes pour supprimer des propriétés.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp::D eleteprops** supprime une ou plusieurs propriétés de l'objet actif. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous n'avez pas besoin d'autoriser la suppression des propriétés de tous les objets. Si l'objet n'est pas modifiable, retournez MAPI_E_NO_ACCESS à partir de la méthode **DeleteProps** . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Il n'est pas nécessaire de définir le type de la propriété pour chaque balise de propriété dans le tableau de balises de propriété pointé par le paramètre _lpPropTagArray_ . Les types de propriétés sont ignorés; Seuls les identificateurs de propriétés sont utilisés. 
  
N'oubliez pas que certains objets ne peuvent pas être modifiés et que ces objets retournent MAPI_E_NO_ACCESS à partir de la méthode **DeleteProps** . D'autres objets permettent de supprimer certaines propriétés, mais pas d'autres. En cas de problème de suppression de certaines propriétés, **DeleteProps** renvoie S_OK. Si vous avez passé un pointeur valide dans le paramètre _lppProblems_ , **DeleteProps** définit le pointeur sur une structure **SPropProblemArray** qui contient des informations détaillées sur les problèmes liés à chaque propriété. Par exemple, si vous supprimez toutes les propriétés d'un message et qu'il y a un problème avec une ou plusieurs de ses pièces jointes, la structure **SPropProblemArray** contiendra une entrée pour l' **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments ](pidtagmessageattachments-canonical-property.md)). 
  
La structure vers laquelle pointe _lppProblems_ n'est valide que si **DeleteProps** renvoie S_OK. Si **DeleteProps** renvoie une erreur, n'essayez pas d'utiliser la structure **SPropProblemArray** . Au lieu de cela, appelez la méthode [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) pour obtenir plus d'informations sur l'erreur. 
  
Libérez la structure **SPropProblemArray** renvoyée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |DeleteProperty  <br/> |MFCMAPI utilise la méthode **IMAPIProp::D eleteprops** pour supprimer une propriété d'un objet.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

