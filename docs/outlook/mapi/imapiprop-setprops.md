---
title: IMAPIPropSetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SetProps
api_type:
- COM
ms.assetid: 49f007c9-42e5-4391-8b83-988c9b0ebdba
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 93bfcce9c45a4c6fd4d57be8c1222be286e0a945
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592030"
---
# <a name="imapipropsetprops"></a>IMAPIProp::SetProps

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Met à jour une ou plusieurs propriétés.
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Paramètres

 _cValues_
  
> [in] Le nombre de valeurs de propriété indiqué par le paramètre _lpPropArray_ . Le paramètre _cValues_ ne doit pas être 0. 
    
 _lpPropArray_
  
> [in] Pointeur vers un tableau de structures [SPropValue](spropvalue.md) qui contiennent des valeurs de propriété à mettre à jour. 
    
 _lppProblems_
  
> [entrée, sortie] À l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; dans le cas contraire, NULL, indiquant ainsi pas besoin d’informations sur l’erreur. Si _lppProblems_ est un pointeur valid en entrée, **SetProps** renvoie des informations détaillées sur les erreurs dans une ou plusieurs propriétés de mise à jour. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Les propriétés ont été correctement mis à jour.
    
Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray** , mais pas en tant que valeurs de retour pour **SetProps**:
  
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.
    
MAPI_E_COMPUTED 
  
> La propriété ne peut pas être mis à jour, car elle est en lecture seule, calculé par le fournisseur de services qui est responsable de l’objet.
    
MAPI_E_INVALID_TYPE 
  
> Le type de propriété n’est pas valide.
    
MAPI_E_NO_ACCESS 
  
> Une tentative a été effectuée pour modifier un objet en lecture seule ou pour accéder à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> La propriété ne peut pas être mis à jour, car elle est supérieure à la taille de mémoire tampon de procédure distante (RPC) d’appel.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Le type de propriété n’est pas le type attendu par l’implémentation d’appel.
    
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Ignorer la balise de propriété **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) et toutes les propriétés de type **PT_ERROR**. N’apportez les modifications ou signaler les problèmes dans la structure **SPropProblemArray** . 
  
Retourner MAPI_E_INVALID_PARAMETER si une propriété de type **PT_OBJECT** est incluse dans le tableau de valeurs de propriété. Aussi renvoyer cette erreur si une propriété à valeurs multiples est incluse dans le tableau et ses membres **cValues** est définie sur 0. 
  
Si l’appel réussit globale, mais il existe des problèmes liés à la définition de certaines des propriétés, qu’elles retournent S_OK et placer les informations sur les problèmes dans l’entrée appropriée de la structure **SPropProblemArray** vers laquelle pointe le paramètre _lppProblems_ . 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Selon le fournisseur de services, vous pourrez également modifier le type de propriété en transmettant une balise de propriété qui contient un type autre que celui utilisé précédemment avec un identificateur de propriété donné.
  
Si vous incluez une balise de propriété pour une propriété qui est pris en charge par l’objet et l’implémentation de **SetProps** permet la création de nouvelles propriétés, la propriété est ajoutée à l’objet. Toute valeur stockée avec l’identificateur de la propriété qui a été utilisé pour la nouvelle propriété est ignorée. 
  
Notez que la valeur de retour de S_OK ne garantit pas que toutes les propriétés ont été correctement mis à jour. Certains fournisseurs de mettre en cache les appels **SetProps** jusqu'à ce qu’ils reçoivent un appel qui nécessite une intervention fournisseur, telles que [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ou [IMAPIProp::GetProps](imapiprop-getprops.md). Par conséquent, il est possible de recevoir des valeurs d’erreur qui sont associées à l’appel **SetProps** avec les appels ultérieurs. 
  
Si **SetProps** renvoie S_OK, vérifiez la structure **SPropProblemArray** désignée par _lppProblems_ les problèmes de mise à jour des propriétés individuelles. Si **SetProps** renvoie une erreur, n’activez pas le tableau de problème de propriétés. Au lieu de cela, appelez la méthode l’objet [IMAPIProp::GetLastError](imapiprop-getlasterror.md) . 
  
Lors de la mise à jour des propriétés de grande taille, **SetProps** peut échouer et renvoyer MAPI_E_NOT_ENOUGH_MEMORY. Il n’existe pas de taille maximale des propriétés et objets différents peuvent avoir différentes limites. Si vous travaillez avec des propriétés potentiellement volumineux, être prêt à appeler la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec IID_IStream l’identificateur d’interface si **SetProps** renvoie cette valeur d’erreur. 
  
Appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de la structure **SPropProblemArray** . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|PropertyEditor.cpp  <br/> |CPropertyEditor::WriteSPropValueToObject  <br/> |MFCMAPI utilise la méthode **IMAPIProp::SetProps** pour écrire dans une propriété à un objet une fois que la propriété a été modifiée.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)

