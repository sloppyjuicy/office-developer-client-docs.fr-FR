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
ms.openlocfilehash: 462d42d68bddba72fd81b97e2aeb9eb5ee8c9c20
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588005"
---
# <a name="imapipropgetprops"></a>IMAPIProp::GetProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère la valeur de propriété d’une ou plusieurs propriétés d’un objet.
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a>Param�tres

 _lpPropTagArray_
  
> [in] Pointeur vers un tableau de balises de propriété qui identifient les propriétés dont les valeurs doivent être récupérés. Le paramètre _lpPropTagArray_ doit être NULL, indiquant que les valeurs de toutes les propriétés de l’objet doivent être retournés, ou point vers une structure [SPropTagArray](sproptagarray.md) qui contient une ou plusieurs balises de propriété. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique le format pour les propriétés dont le type PT_UNSPECIFIED. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les valeurs de chaîne pour ces propriétés doivent être retournées au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les valeurs de chaîne doivent être retournées au format ANSI.
    
 _lpcValues_
  
> [out] Un pointeur vers un nombre de valeurs de propriété indiqué par le paramètre _lppPropArray_ . Si _lppPropArray_ est NULL, le contenu du paramètre _lpcValues_ est égale à zéro. 
    
 _lppPropArray_
  
> [out] Pointeur vers un pointeur vers les valeurs des propriétés récupérées.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les valeurs de propriété ont été récupérés correctement.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais une ou plusieurs propriétés ne sont pas accessible. Le membre **aulPropTag** de la valeur de propriété pour chaque propriété non disponible a un type de propriété de PT_ERROR et d’un identificateur de zéro. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
    
MAPI_E_INVALID_PARAMETER 
  
> Zéro a été passée dans le membre **cValues** de la structure **SPropTagArray** désigné par _lpPropTagArray_.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp::GetProps** Obtient les valeurs de propriété d’une ou plusieurs propriétés d’un objet. 
  
Les valeurs de propriété sont retournés dans le même ordre lorsqu’elles ont été demandées (autrement dit, l’ordre des propriétés de tableau de la propriété tag désignés par correspondances _lpPropTagArray_ l’ordre dans le tableau des structures de valeur de propriété désignés par _lppPropArray _). 
  
Les types de propriétés spécifiés dans les membres **aulPropTag** du tableau de balise de propriété indiquent le type de valeur doit être retournée dans le membre de la **valeur** de chaque structure de valeur de propriété. Toutefois, si l’appelant ne connaît pas le type d’une propriété, le type du membre **aulPropTag** peut avoir à la place PT_UNSPECIFIED. L’extraction de la valeur, **GetProps** définit le type approprié dans le membre **aulPropTag** de la structure de valeur de propriété pour la propriété. 
  
Si les types de propriété sont spécifiés dans le **SPropTagArray** dans _lpPropTagArray_, les valeurs de propriété dans le **SPropValue** renvoyé dans _lppPropArray_ dont les types correspondent exactement les types demandés, sauf si une valeur d’erreur est renvoyée. à la place. 
  
Propriétés de type chaîne peuvent avoir une des deux types de propriétés : PT_UNICODE pour représenter le format Unicode et PT_STRING8 pour représenter le format ANSI. Si l’indicateur MAPI_UNICODE est défini dans le paramètre _ulFlags_ , chaque fois que **GetProps** ne peut pas déterminer le format approprié pour une propriété de chaîne, elle renvoie la valeur dans le format Unicode. **GetProps** ne peut pas déterminer le type de propriété une chaîne exacte dans les situations suivantes : 
  
- Le paramètre _lpPropTagArray_ est défini sur la valeur NULL à toutes les propriétés de la requête. 
    
- Le membre **aulPropTag** inclut la valeur PT_UNSPECIFIED en tant que tableau de la propriété tag, son type de propriété. 
    
Si le paramètre _lpPropTagArray_ est défini sur NULL pour récupérer toutes les propriétés de l’objet et aucune propriété n’existe, **GetProps** effectue les opérations suivantes : 
  
- Renvoie S_OK.
    
- Définit la valeur de nombre dans le membre **cValues** de la structure de valeur de propriété sur 0. 
    
- Définit le contenu de _lpcValues_ à 0. 
    
- Définit _lppPropArray_ sur NULL. 
    
 **GetProps** ne doit pas retourner de propriétés à plusieurs valeurs avec **cValues** défini sur 0. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Appelez la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) pour allouer de la mémoire à l’origine de la structure [SPropValue](spropvalue.md) désignée par _lpPropTagArray_; Appelez [MAPIAllocateMore](mapiallocatemore.md) pour allouer de mémoire supplémentaire nécessaire pour les membres de la structure. 
  
Retourner MAPI_W_ERRORS_RETURNED si vous ne peut pas récupérer la valeur pour une ou plusieurs des propriétés demandées. Dans la structure de valeur de propriété, définissez le type de membre **aulPropTag** à PT_ERROR et le membre de la **valeur** d’un code d’état qui décrit l’erreur. Par exemple, si vous disposez convertir une chaîne Unicode et ne prennent pas en charge Unicode, définissez le membre de **valeur** pour MAPI_E_BAD_CHARWIDTH. Si la propriété est trop importante, affectez-lui MAPI_E_NOT_ENOUGH_MEMORY. Si l’objet ne prend pas en charge la propriété, affectez-lui MAPI_E_NOT_FOUND. 
  
Implémentation d’un fournisseur de transport à distance de la méthode **GetProps** doit renvoyer les valeurs des propriétés du dossier pour les propriétés requises par l’appelant. Votre implémentation procédez comme suit : 
  
- Allouez un tableau de valeurs de propriété pour revenir à l’appelant et stocker son adresse dans le paramètre de pointeur de la propriété value transmis à cet effet.
    
- Copiez les balises de propriété à partir des propriétés du dossier dans les balises de propriété dans le tableau de valeurs de propriété en fonction du tableau des balises de propriété transmis à **GetProps**.
    
- Assurez-vous que le type de propriété est défini pour toutes les balises de propriété transmis à **GetProps**. L’appelant peut passer un type de propriété de PT_UNSPECIFIED, dans lequel cas **GetProps** doit définir le type de propriété correcte de cette balise de propriété. 
    
- Définissez la valeur de chaque propriété dans le tableau de valeurs de propriété en fonction de sa balise. Par exemple, si la balise de propriété demandée par l’appelant est **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** pouvez définir la valeur à MAPI_FOLDER. 
    
- Si l’appelant passe les balises de propriété que votre implémentation ne gère pas, vous pouvez définir la balise de propriété sur PT_ERROR pour ces propriétés et définir la valeur de propriété à MAPI_E_NOT_FOUND.
    
- Renvoie S_OK si aucune erreur ne s’est produite ou MAPI_W_ERRORS_RETURNED si des erreurs.
    
Implémentation d’un fournisseur de transport à distance de la méthode **GetProps** doit prendre en charge les propriétés suivantes au minimum : 
  
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
    
## <a name="notes-to-callers"></a>Notes aux appelants

Pour les propriétés de type PT_OBJECT, appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) au lieu de **GetProps**. 
  
Pour les propriétés d’informations sécurisé, ne prévoyez pas les récupérer en appelant **GetProps** avec le paramètre _lppPropTagArray_ la valeur NULL. Vous devez définir explicitement identificateur d’une propriété sécurisée dans le membre **aulPropTag** de son groupe de balise de propriété lorsque vous appelez **GetProps**. Quand et comment une propriété sécurisée est disponible dépend du fournisseur de services. 
  
Libérer la structure **SPropValue** retournée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) uniquement si **GetProps** renvoie S_OK ou MAPI_W_ERRORS_RETURNED. 
  
Si **GetProps** renvoie MAPI_W_ERRORS_RETURNED, car il ne peut pas accéder une ou plusieurs propriétés, vérifiez les balises de propriété des propriétés renvoyées. Les propriétés ayant échouées auront les valeurs suivantes définies dans leur structure de valeur de propriété : 
  
- Le type de propriété dans le membre **aulPropTag** défini sur PT_ERROR. 
    
- La valeur de propriété dans le membre de la **valeur** est définie sur un code d’état de l’erreur, tel que MAPI_E_NOT_FOUND. 
    
Propriétés qui échouent, car ils sont trop grandes pour être facilement retourné dans la structure de valeur de propriété ont leurs membres **valeur** MAPI_E_NOT_ENOUGH_MEMORY. En règle générale, cela produit à des propriétés de type chaîne ou binaire PT_STRING8, PT_UNICODE ou PT_BINARY lorsque la valeur de la propriété est 4 Ko ou plus. Appelez **IMAPIProp::OpenProperty** pour récupérer les propriétés de grande taille. 
  
Pas toutes les implémentations de **GetProps** prend en charge les formats ANSI et Unicode pour des chaînes de caractères. Lorsqu’une propriété particulière nécessite la conversion du format de chaîne et **GetProps** ne peut pas prendre en charge, le membre de la **valeur** de la propriété est défini sur MAPI_E_BAD_CHARWIDTH. 
  
Pour vérifier si un fichier PST est un fichier PST SharePoint, montez le fichier PST à l’aide [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), puis d’appeler **GetProps** sur l’objet de banque de message demandant cette propriété. S’il existe, vous pouvez supposer que le fichier PST a été configuré pour SharePoint. Si ce n’est pas le cas, le fichier PST n’a pas été configuré comme un fichier PST SharePoint. 
  
Pour plus d’informations sur l’utilisation de **GetProps** pour accéder aux propriétés, voir [Extraction des propriétés MAPI](retrieving-mapi-properties.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI utilise la méthode **IMAPIProp::GetProps** pour obtenir toutes les propriétés d’un objet en passant le tableau renvoyé par la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) dans le paramètre _lpPropTagArray_ ou NULL.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Récupération des propriétés MAPI](retrieving-mapi-properties.md)
  
[Utilisation de Macros pour la gestion des erreurs](using-macros-for-error-handling.md)

