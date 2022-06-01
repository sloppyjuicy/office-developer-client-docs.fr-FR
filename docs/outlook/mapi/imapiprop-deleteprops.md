---
title: IMAPIPropDeleteProps
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPIPropDeleteProps, qui supprime une ou plusieurs propriétés d’un objet.
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
ms.openlocfilehash: 76a4c02634df03ed6177a00d1d04ba4195f2e273
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816604"
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
  
> [in] Pointeur vers un tableau de balises de propriétés qui indiquent les propriétés à supprimer. Le membre **cValues** de la structure [SPropTagArray](sproptagarray.md) pointée par  _lpPropTagArray_ ne doit pas être égal à zéro et le paramètre  _lpPropTagArray_ lui-même ne doit pas être NULL. 
    
 _lppProblems_
  
> [in, out] Lors de l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; sinon, NULL, qui indique qu’il n’est pas nécessaire d’obtenir des informations d’erreur. Si  _lppProblems_ est un pointeur valide sur l’entrée, **DeleteProps** retourne des informations détaillées sur les erreurs lors de la suppression d’une ou de plusieurs propriétés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les propriétés ont été supprimées avec succès.
    
MAPI_E_NO_ACCESS 
  
> L’appelant dispose d’autorisations insuffisantes pour supprimer des propriétés.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp::D eleteProps** supprime une ou plusieurs propriétés de l’objet actuel. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous n’avez pas besoin d’autoriser la suppression de propriétés de tous les objets. Si l’objet n’est pas modifiable, renvoyez MAPI_E_NO_ACCESS à partir de la méthode **DeleteProps** . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous n’avez pas besoin de définir le type de propriété pour chaque balise de propriété dans le tableau de balises de propriétés pointé par le paramètre  _lpPropTagArray_ . Les types de propriétés sont ignorés ; seuls les identificateurs de propriété sont utilisés. 
  
Sachez que certains objets n’autorisent pas la modification et que ces objets retournent MAPI_E_NO_ACCESS de la méthode **DeleteProps** . D’autres objets permettent de supprimer certaines propriétés, mais pas d’autres. En cas de problème lors de la suppression de certaines propriétés uniquement, **DeleteProps** retourne S_OK. Si vous avez passé un pointeur valide dans le paramètre _lppProblems_ , **DeleteProps** définit le pointeur sur une structure **SPropProblemArray** qui contient des informations détaillées sur les problèmes liés à chaque propriété. Par exemple, si vous supprimez toutes les propriétés d’un message et qu’il existe un problème avec une ou plusieurs de ses pièces jointes, la structure **SPropProblemArray** contient une entrée pour la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
La structure pointée par  _lppProblems_ n’est valide que si **DeleteProps** retourne S_OK. Si **DeleteProps** retourne une erreur, n’essayez pas d’utiliser la structure **SPropProblemArray** . Appelez plutôt la méthode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) de l’objet pour obtenir plus d’informations sur l’erreur. 
  
Libérez la structure **SPropProblemArray** retournée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |DeleteProperty  <br/> |MFCMAPI utilise la méthode **IMAPIProp::D eleteProps** pour supprimer une propriété d’un objet. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

