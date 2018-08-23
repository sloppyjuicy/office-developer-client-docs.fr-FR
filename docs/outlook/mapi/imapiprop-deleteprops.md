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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a0d86b9b0342beea6b33db0219cb5889d2e63f03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592072"
---
# <a name="imapipropdeleteprops"></a>IMAPIProp::DeleteProps

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Supprime une ou plusieurs propriétés d’un objet. 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Param�tres

 _lpPropTagArray_
  
> [in] Pointeur vers un tableau de balises de propriété qui indiquent les propriétés à supprimer. Le membre **cValues** de la structure [SPropTagArray](sproptagarray.md) désigné par _lpPropTagArray_ ne doit pas être zéro, et le paramètre _lpPropTagArray_ lui-même ne doit pas être NULL. 
    
 _lppProblems_
  
> [entrée, sortie] À l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; dans le cas contraire, la valeur NULL, ce qui indique qu’il n’est pas nécessaire pour les informations d’erreur. Si _lppProblems_ est un pointeur valid en entrée, **DeleteProps** renvoie des informations détaillées sur les erreurs lors de la suppression d’une ou plusieurs propriétés. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Les propriétés ont été supprimées.
    
MAPI_E_NO_ACCESS 
  
> L’appelant a des autorisations suffisantes pour supprimer des propriétés.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp::DeleteProps** supprime une ou plusieurs propriétés de l’objet actif. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Il est inutile que les propriétés doivent être supprimés de tous les objets. Si l’objet n’est pas modifiable, renvoyer MAPI_E_NO_ACCESS à partir de la méthode **DeleteProps** . 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous n’êtes pas obligé de définir le type de propriété de chaque balise de propriété dans le tableau de balise de propriété indiqué par le paramètre _lpPropTagArray_ . Types de propriété sont ignorées ; uniquement les identificateurs de propriété sont utilisés. 
  
Sachez que certains objets ne permettent pas de modification et que ces objets retournent MAPI_E_NO_ACCESS à partir de la méthode **DeleteProps** . Autres objets permettent de certaines propriétés d’être supprimé, mais pas à d’autres. Lorsqu’il existe un problème de suppression de certaines propriétés, **DeleteProps** renvoie S_OK. Si vous avez passé un pointeur valide dans le paramètre _lppProblems_ , **DeleteProps** définira le pointeur vers une structure **SPropProblemArray** qui contient des informations détaillées sur les problèmes liés à chaque propriété. Par exemple, si vous supprimez toutes les propriétés d’un message et il existe un problème avec un ou plusieurs de ses pièces jointes, la structure **SPropProblemArray** contient une entrée pour le **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments ](pidtagmessageattachments-canonical-property.md)) propriété. 
  
La structure vers laquelle pointée _lppProblems_ est valide uniquement si **DeleteProps** renvoie S_OK. Si **DeleteProps** renvoie une erreur, n’essayez pas d’utiliser la structure **SPropProblemArray** . Au lieu de cela, appelez la méthode l’objet [IMAPIProp::GetLastError](imapiprop-getlasterror.md) pour obtenir plus d’informations sur l’erreur. 
  
Libérez de la structure **SPropProblemArray** retournée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |DeleteProperty  <br/> |MFCMAPI utilise la méthode **IMAPIProp::DeleteProps** pour supprimer une propriété d’un objet.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

