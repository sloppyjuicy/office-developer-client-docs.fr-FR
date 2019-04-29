---
title: IMAPIPropGetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetProps
api_type:
- COM
ms.assetid: 1c7a9cd2-d765-4218-9aee-52df1a2aae6c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9b03775d495f7d1f51142eb0ed06fc9ecdf6d1a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412456"
---
# <a name="imapipropgetprops"></a>IMAPIProp::GetProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère la valeur de propriété d'une ou de plusieurs propriétés d'un objet.
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a>Paramètres

 _lpPropTagArray_
  
> dans Pointeur vers un tableau de balises de propriété qui identifient les propriétés dont les valeurs doivent être récupérées. Le paramètre _lpPropTagArray_ doit être null, ce qui indique que les valeurs de toutes les propriétés de l'objet doivent être renvoyées ou pointer vers une structure [SPropTagArray](sproptagarray.md) qui contient une ou plusieurs balises de propriété. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui indique le format des propriétés ayant le type PT_UNSPECIFIED. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les valeurs de chaîne de ces propriétés doivent être renvoyées au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les valeurs de chaîne doivent être renvoyées au format ANSI.
    
 _lpcValues_
  
> remarquer Pointeur vers le nombre de valeurs de propriété vers lesquelles pointe le paramètre _lppPropArray_ . Si _lppPropArray_ est null, le contenu du paramètre _lpcValues_ est zéro. 
    
 _lppPropArray_
  
> remarquer Pointeur vers un pointeur vers les valeurs de propriété récupérées.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les valeurs de propriété ont été correctement récupérées.
    
MAPI_W_ERRORS_RETURNED 
  
> L'appel a réussi globalement, mais une ou plusieurs propriétés sont inaccessibles. Le membre **aulPropTag** de la valeur de propriété pour chaque propriété indisponible a un type de propriété PT_ERROR et un identificateur de zéro. Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
MAPI_E_INVALID_PARAMETER 
  
> Zéro a été transmis dans le membre **cValues** de la structure **SPropTagArray** vers laquelle pointe _lpPropTagArray_.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp:: GetProps** obtient les valeurs de propriété d'une ou de plusieurs propriétés d'un objet. 
  
Les valeurs de propriété sont renvoyées dans le même ordre que celui demandé (c'est-à-dire, l'ordre des propriétés dans le tableau de balises de propriété vers lequel pointe _lpPropTagArray_ correspond à l'ordre dans le tableau de structures de valeurs de propriétés pointé par _lppPropArray _). 
  
Les types de propriétés spécifiés dans les membres **aulPropTag** du tableau de balises de propriété indiquent le type de valeur à renvoyer dans le membre de **valeur** de chaque structure de valeur de propriété. Toutefois, si l'appelant ne connaît pas le type d'une propriété, le type dans le membre **aulPropTag** peut être défini à la place de PT_UNSPECIFIED. Lors de la récupération de la valeur, **GetProps** définit le type correct dans le membre **aulPropTag** de la structure de valeur de la propriété pour la propriété. 
  
Si les types de propriété sont spécifiés dans le **SPropTagArray** dans _lpPropTagArray_, les valeurs de propriété dans les **SPropValue** renvoyées dans _lppPropArray_ ont des types qui correspondent exactement aux types demandés, sauf si une valeur d'erreur est renvoyée. cas. 
  
Les propriétés de chaîne peuvent avoir l'un des deux types de propriété suivants: PT_UNICODE pour représenter le format Unicode et PT_STRING8 pour représenter le format ANSI. Si l'indicateur MAPI_UNICODE est défini dans le paramètre _ulFlags_ , chaque fois que **GetProps** ne peut pas déterminer le format approprié pour une propriété de chaîne, il renvoie sa valeur au format Unicode. **GetProps** ne peut pas déterminer un type de propriété de chaîne exact dans les situations suivantes: 
  
- Le paramètre _lpPropTagArray_ est défini sur null pour demander toutes les propriétés. 
    
- Le membre **aulPropTag** inclut la valeur PT_UNSPECIFIED comme type de propriété dans le tableau de balises de propriété. 
    
Si le paramètre _lpPropTagArray_ est défini sur null pour récupérer toutes les propriétés de l'objet et qu'aucune propriété n'existe, **GetProps** effectue les opérations suivantes: 
  
- Renvoie S_OK.
    
- Affecte la valeur 0 à la valeur Count dans le membre **cValues** de la structure de la valeur de la propriété. 
    
- Définit le contenu de _lpcValues_ sur 0. 
    
- Définit _lppPropArray_ sur null. 
    
 **GetProps** ne doit pas renvoyer les propriétés à valeurs multiples avec **cValues** défini sur 0. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Appelez la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) pour allouer initialement de la mémoire pour la structure [SPropValue](spropvalue.md) vers laquelle pointe _lpPropTagArray_; Appelez [MAPIAllocateMore](mapiallocatemore.md) pour allouer toute mémoire supplémentaire nécessaire pour les membres de la structure. 
  
Renvoie MAPI_W_ERRORS_RETURNED si vous ne pouvez pas récupérer la valeur d'une ou plusieurs des propriétés demandées. Dans la structure de la valeur de la propriété, définissez le type dans le membre **aulPropTag** sur PT_ERROR et le membre **value** sur un code d'État qui décrit l'erreur. Par exemple, si vous devez convertir une chaîne au format Unicode et ne pas prendre en charge Unicode, définissez le membre **value** sur MAPI_E_BAD_CHARWIDTH. Si la propriété est trop volumineuse, définissez-la sur MAPI_E_NOT_ENOUGH_MEMORY. Si l'objet ne prend pas en charge la propriété, affectez-lui la valeur MAPI_E_NOT_FOUND. 
  
L'implémentation d'un fournisseur de transport distant de la méthode **GetProps** doit renvoyer les valeurs de propriété du dossier pour les propriétés demandées par l'appelant. Votre implémentation doit effectuer les opérations suivantes: 
  
- AlLouez un tableau de valeurs de propriété à renvoyer à l'appelant et stockez son adresse dans le paramètre de pointeur de valeur de propriété transmis à cet effet.
    
- Copiez les balises de propriété des propriétés du dossier dans les balises de propriété du tableau de valeurs de propriété en fonction du tableau de balises de propriété transmises à **GetProps**.
    
- Assurez-vous que le type de propriété est défini pour toutes les balises de propriété transmises à **GetProps**. L'appelant peut transmettre un type de propriété PT_UNSPECIFIED, auquel cas **GetProps** doit définir le type de propriété approprié pour cette balise de propriété. 
    
- Définissez la valeur de chaque propriété dans le tableau de valeurs de la propriété en fonction de sa balise. Par exemple, si la balise de propriété demandée par l'appelant est **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** pouvez définir la valeur sur MAPI_FOLDER. 
    
- Si l'appelant transmet les balises de propriété que votre implémentation ne gère pas, vous pouvez définir la balise de propriété sur PT_ERROR pour ces propriétés et définir la valeur de la propriété sur MAPI_E_NOT_FOUND.
    
- Renvoie S_OK si aucune erreur ne s'est produite ou MAPI_W_ERRORS_RETURNED s'il y a eu des erreurs.
    
L'implémentation d'un fournisseur de transport distant de la méthode **GetProps** doit au minimum prendre en charge les propriétés suivantes: 
  
- **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))
    
- **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))
    
- **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_OBJECT_TYPE**
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour les propriétés de type PT_OBJECT, appelez la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) au lieu de **GetProps**. 
  
Pour les propriétés sécurisées, ne prévoyez pas de les récupérer en appelant **GetProps** avec le paramètre _LPPPROPTAGARRAY_ défini sur null. Vous devez définir explicitement l'identificateur d'une propriété sécurisée dans le membre **aulPropTag** de son tableau de balises de propriété lorsque vous appelez **GetProps**. Le fournisseur de services indique quand et comment une propriété sécurisée est disponible. 
  
Libérez la structure **SPropValue** renvoyée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) uniquement si **GetProps** renvoie S_OK ou MAPI_W_ERRORS_RETURNED. 
  
Si **GetProps** renvoie MAPI_W_ERRORS_RETURNED car il n'a pas accès à une ou plusieurs propriétés, vérifiez les balises de propriété des propriétés renvoyées. Les valeurs suivantes sont définies dans la structure de la valeur de la propriété des propriétés ayant échoué: 
  
- Type de propriété dans le membre **aulPropTag** défini sur PT_ERROR. 
    
- La valeur de la propriété dans le membre de la **valeur** est définie sur un code d'État pour l'erreur, par exemple MAPI_E_NOT_FOUND. 
    
Les propriétés qui échouent, car elles sont trop volumineuses pour être renvoyées dans la structure de la valeur de la propriété, leur membre de **valeur** est défini sur MAPI_E_NOT_ENOUGH_MEMORY. En règle générale, cela se produit avec les propriétés de chaîne ou binaires de type PT_STRING8, PT_UNICODE ou PT_BINARY lorsque la valeur de la propriété est supérieure ou égale à 4 Ko. Appelez **IMAPIProp:: OpenProperty** pour récupérer les propriétés volumineuses. 
  
Toutes les implémentations de **GetProps** prennent en charge les formats Unicode et ANSI pour les chaînes de caractères. Lorsqu'une propriété particulière requiert une conversion de format de chaîne et que **GetProps** ne peut pas la prendre en charge, le membre de **valeur** de la propriété est défini sur MAPI_E_BAD_CHARWIDTH. 
  
Pour vérifier s'il s'agit d'un fichier PST SharePoint, montez-le à l'aide de [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md), puis appelez **GetProps** sur l'objet de banque de messages pour demander cette propriété. S'il existe, vous pouvez supposer que le fichier PST a été configuré pour SharePoint; Si ce n'est pas le cas, le fichier PST n'a pas été configuré en tant que fichier PST SharePoint. 
  
Pour plus d'informations sur l'utilisation de **GetProps** pour accéder aux propriétés, consultez la rubrique [extraction de propriétés MAPI](retrieving-mapi-properties.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI utilise la méthode **IMAPIProp:: GetProps** pour obtenir toutes les propriétés d'un objet en passant null ou le tableau renvoyé par la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) dans le paramètre _lpPropTagArray_ .  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Récupération des propriétés MAPI](retrieving-mapi-properties.md)
  
[Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

