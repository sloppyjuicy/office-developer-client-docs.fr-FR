---
title: IMAPIPropGetNamesFromIDs
description: IMAPIPropGetNamesFromIDs fournit les noms de propriété qui correspondent à un ou plusieurs identificateurs de propriété.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.GetNamesFromIDs
api_type:
- COM
ms.assetid: 3efa4731-cf32-4a6c-9ba8-d059e58b0d98
ms.openlocfilehash: cce53f472565ae0f90cc22024a636244ad4cabae
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816814"
---
# <a name="imapipropgetnamesfromids"></a>IMAPIProp::GetNamesFromIDs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit les noms de propriétés qui correspondent à un ou plusieurs identificateurs de propriété.
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a>Paramètres

 _lppPropTags_
  
> [in, out] Lors de l’entrée, pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriétés ; sinon, NULL, indiquant que tous les noms doivent être retournés. Le membre **cValues** du tableau de balises de propriétés ne peut pas être 0. Si  _lppPropTags_ est un pointeur valide sur l’entrée, **GetNamesFromIDs** retourne les noms de chaque identificateur de propriété inclus dans le tableau. 
    
 _lpPropSetGuid_
  
> [in] Pointeur vers un GUID, ou structure [GUID](guid.md) , qui identifie un jeu de propriétés. Le paramètre  _lpPropSetGuid_ peut pointer vers un jeu de propriétés valide ou être NULL. 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui indique le type de noms à retourner. Les indicateurs suivants peuvent être utilisés (si les deux indicateurs sont définis, aucun nom n’est retourné) :
    
MAPI_NO_IDS 
  
> Demande que seuls les noms stockés sous forme de chaînes Unicode soient retournés. 
    
MAPI_NO_STRINGS 
  
> Demande que seuls les noms stockés en tant qu’identificateurs numériques soient retournés. 
    
 _lpcPropNames_
  
> [out] Pointeur vers un nombre de pointeurs de nom de propriété dans le tableau pointé par le paramètre  _lppPropNames_ . 
    
 _lpppPropNames_
  
> [out] Pointeur vers un tableau de pointeurs vers des structures [MAPINAMEID](mapinameid.md) qui contiennent des noms de propriétés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les noms des propriétés ont été retournés avec succès. 
    
MAPI_E_NO_SUPPORT 
  
> L’objet ne prend pas en charge les propriétés nommées. 
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi dans l’ensemble, mais les noms d’une ou plusieurs propriétés n’ont pas pu être retournés. Les balises de propriété pour les propriétés défaillantes ont un type de propriété **de PT_ERROR**. Lorsque cet avertissement est retourné, l’appel doit être traité comme ayant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md). 
    
MAPI_E_INVALID_PARAMETER 
  
> Le membre **cValues** d’une ou plusieurs des entrées dans le tableau de balises de propriétés pointé par  _lppPropTags_ est défini sur 0. 
    
## <a name="remarks"></a>Remarques

Bien que l’accès à la plupart des propriétés soit par identificateur de propriété, certaines propriétés sont accessibles par nom. La méthode **IMAPIProp::GetNamesFromIDs** peut être appelée pour effectuer les opérations suivantes : 
  
- Récupérez les noms des identificateurs de propriétés spécifiques dans un jeu de propriétés spécifique.
    
- Récupérez les noms des identificateurs de propriétés spécifiques dans n’importe quel jeu de propriétés.
    
- Récupérez les noms de toutes les propriétés nommées incluses dans le mappage de l’objet.
    
Si  _lppPropTags_ pointe vers un tableau de balises de propriétés valide avec un ou plusieurs identificateurs de propriétés et  _que lpPropSetGuid_ pointe vers un jeu de propriétés valide, **GetNamesFromIDs** ignore le jeu de propriétés et les types de propriétés et retourne tous les noms mappés aux identificateurs spécifiés. 
  
Si  _lppPropTags_ pointe vers un tableau de balises de propriétés valide avec un ou plusieurs identificateurs de propriété et  _que lpPropSetGuid_ a la valeur NULL, **GetNamesFromIDs** retourne tous les noms mappés aux identificateurs spécifiés. 
  
Si un identificateur spécifié n’a pas de nom, **GetNamesFromIDs** retourne NULL à la place de cet identificateur dans la structure retournée dans  _lpppPropNames_ et retourne également MAPI_W_ERRORS_RETURNED. 
  
Si  _lpPropSetGuid_ et  _lppPropTags_ sont null, **GetNamesFromIDs alloue** un nouveau tableau de balises de propriétés et retourne tous les noms de toutes les propriétés nommées pour l’objet. 
  
Lorsqu’il n’y a aucun nom à renvoyer, peut-être parce qu’il n’y a aucune propriété dans le jeu de propriétés demandé ou que toutes les propriétés sont d’un type exclu par les indicateurs, **GetNamesFromIDs effectue les opérations suivantes** : 
  
- Retourne S_OK.
    
- Alloue une nouvelle structure **SPropTagArray** , en définissant le membre **cValues sur** 0. 
    
- Définit le contenu de  _lpcPropNames sur_ 0. 
    
- Définit le contenu de  _lpppPropNames sur_ NULL. 
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si  _lpPropSetGuid_ pointe vers un jeu de  _propriétés valide et que lppPropTags_ a la valeur NULL, le résultat n’est pas défini. Vous pouvez utiliser l’une des stratégies suivantes : 
  
- Ignorez le jeu de propriétés et retournez les noms des identificateurs dans le tableau de balises de propriétés.
    
- Retournez uniquement les noms des identificateurs dans le tableau de balises de propriétés qui appartiennent au jeu de propriétés spécifié.
    
- Échec de l’appel, en retournant MAPI_E_INVALID_PARAMETER. 
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour récupérer toutes les propriétés nommées d’un objet, vous devez d’abord appeler la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) de l’objet, puis passer les identificateurs retournés qui se trouvent au-dessus de la plage de 0x8000 à **GetNamesFromIDs**.
  
Si vous passez un jeu de propriétés valide, mais pas un tableau de balises de propriétés valide, préparez-vous à des résultats imprévisibles. Certaines implémentations de **GetNamesFromID ignorent** le jeu de propriétés et retournent les noms des identificateurs dans le tableau de balises de propriétés. Certaines implémentations retournent MAPI_E_INVALID_PARAMETER. D’autres implémentations retournent encore des noms pour les identificateurs de toutes les propriétés du jeu de propriétés. Si l’ensemble de propriétés est PS_PUBLIC_STRINGS, **GetNamesFromIDs** peut retourner tous les noms qui ont été créés. Le fait que le fournisseur de services stocke une propriété sous les identificateurs associés aux chaînes publiques n’est pas important. 
  
Une fois les noms de propriété terminés, vérifiez le contenu du paramètre  _lpcPropNames_ pour déterminer si des noms ont été retournés. Si c’est le cas, appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer la mémoire pointée par  _lppPropTags_ et  _lpppPropNames_ lorsqu’un résultat réussi est retourné. Un appel à **MAPIFreeBuffer** suffit pour chaque paramètre ; vous n’avez pas besoin de parcourir le tableau de pointeurs et de libérer chaque structure **MAPINAMEID** individuellement. 
  
Pour plus d’informations sur les propriétés nommées, consultez [Propriétés nommées MAPI](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedProps  <br/> |MFCMAPI utilise la méthode **IMAPIProp::GetNamesFromIDs pour rechercher les propriétés** nommées qui ont été mappées précédemment. |
   
## <a name="see-also"></a>Voir aussi



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)
  
[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPINAMEID](mapinameid.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[MAPI des propri�t�s nomm�e](mapi-named-properties.md)
  
[Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

