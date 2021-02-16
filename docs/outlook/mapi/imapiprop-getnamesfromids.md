---
title: IMAPIPropGetNamesFromIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetNamesFromIDs
api_type:
- COM
ms.assetid: 3efa4731-cf32-4a6c-9ba8-d059e58b0d98
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f6688afde9b36a7722eaaf768f091481c15b7308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423572"
---
# <a name="imapipropgetnamesfromids"></a>IMAPIProp::GetNamesFromIDs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit les noms de propriété qui correspondent à un ou plusieurs identificateurs de propriété.
  
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
  
> [in, out] Lors de l’entrée, un pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété ; sinon, NULL, indiquant que tous les noms doivent être renvoyés. Le **membre cValues** du tableau de balises de propriétés ne peut pas être 0. Si  _lppPropTags est_ un pointeur valide lors de l’entrée, **GetNamesFromIDs** renvoie les noms de chaque identificateur de propriété inclus dans le tableau. 
    
 _lpPropSetGuid_
  
> [in] Pointeur vers un GUID ou une structure [GUID](guid.md) qui identifie un jeu de propriétés. Le  _paramètre lpPropSetGuid_ peut pointer vers un jeu de propriétés valide ou peut être NULL. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique le type de noms à retourner. Les indicateurs suivants peuvent être utilisés (si les deux indicateurs sont définies, aucun nom ne sera renvoyé) :
    
MAPI_NO_IDS 
  
> Demande que seuls les noms stockés en tant que chaînes Unicode soient renvoyés. 
    
MAPI_NO_STRINGS 
  
> Demande que seuls les noms stockés en tant qu’identificateurs numériques soient renvoyés. 
    
 _lpcPropNames_
  
> [out] Pointeur vers un nombre de pointeurs de nom de propriété dans le tableau pointé par _le paramètre lppPropNames._ 
    
 _lpppPropNames_
  
> [out] Pointeur vers un tableau de pointeurs vers des structures [MAPINAMEID](mapinameid.md) qui contiennent des noms de propriétés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les noms des propriétés ont été renvoyés avec succès. 
    
MAPI_E_NO_SUPPORT 
  
> L’objet ne prend pas en charge les propriétés nommées. 
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi globalement, mais les noms d’une ou plusieurs propriétés n’ont pas pu être renvoyés. Les balises de propriété pour les propriétés défaillantes ont un type de propriété **PT_ERROR**. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED.** Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md) 
    
MAPI_E_INVALID_PARAMETER 
  
> Le **membre cValues** d’une ou plusieurs des entrées du tableau de balises de propriétés pointées par  _lppPropTags_ est définie sur 0. 
    
## <a name="remarks"></a>Remarques

Bien que l’accès à la plupart des propriétés se fait par identificateur de propriété, certaines propriétés sont accessibles par nom. La **méthode IMAPIProp::GetNamesFromIDs** peut être appelée pour : 
  
- Récupérer les noms des identificateurs de propriété spécifiques dans un jeu de propriétés spécifique.
    
- Récupérer les noms des identificateurs de propriété spécifiques dans n’importe quel jeu de propriétés.
    
- Récupérer les noms de toutes les propriétés nommées incluses dans le mappage de l’objet.
    
Si  _lppPropTags_ pointe vers un tableau de balises de propriétés valide avec un ou plusieurs identificateurs de propriété et  _que lpPropSetGuid_ pointe vers un jeu de propriétés valide, **GetNamesFromIDs** ignore le jeu de propriétés et les types de propriétés et renvoie tous les noms qui sont mappés aux identificateurs spécifiés. 
  
Si  _lppPropTags_ pointe vers un tableau de balises de propriétés valide avec un ou plusieurs identificateurs de propriété et  _que lpPropSetGuid_ a la valeur NULL, **GetNamesFromIDs** renvoie tous les noms mappés aux identificateurs spécifiés. 
  
Si un identificateur spécifié n’a pas de nom, **GetNamesFromIDs** renvoie la valeur NULL à la place de cet identificateur dans la structure renvoyée dans  _lpppPropNames_ et renvoie également MAPI_W_ERRORS_RETURNED. 
  
Si  _lpPropSetGuid_ et  _lppPropTags_ ont la valeur NULL, **GetNamesFromIDs** alloue un nouveau tableau de balises de propriétés et renvoie tous les noms de toutes les propriétés nommées de l’objet. 
  
Lorsqu’il n’y a aucun nom à retourner, peut-être parce qu’il n’y a aucune propriété dans le jeu de propriétés demandé ou que toutes les propriétés sont d’un type exclu par les indicateurs, **GetNamesFromIDs** : 
  
- Renvoie S_OK.
    
- Alloue une nouvelle structure **SPropTagArray,** en fixant le membre **cValues** sur 0. 
    
- Définit le contenu de  _lpcPropNames_ sur 0. 
    
- Définit le contenu de  _lpppPropNames_ sur NULL. 
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si  _lpPropSetGuid_ pointe vers un jeu de propriétés valide et  _que lppPropTags_ est NULL, le résultat n’est pas définie. Vous pouvez utiliser l’une des stratégies suivantes : 
  
- Ignorez le jeu de propriétés et renvoyer les noms des identificateurs dans le tableau de balises de propriétés.
    
- Renvoyer les noms des identificateurs du tableau de balises de propriétés qui appartiennent au jeu de propriétés spécifié.
    
- Échec de l’appel, renvoyant MAPI_E_INVALID_PARAMETER. 
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour récupérer toutes les propriétés nommées d’un objet, vous devez d’abord appeler la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) de l’objet, puis transmettre les identificateurs renvoyés au-dessus de la plage 0x8000 à **GetNamesFromIDs**.
  
Si vous passez un jeu de propriétés valide mais pas un tableau de balises de propriétés valide, soyez préparé pour des résultats imprévisibles. Certaines implémentations **de GetNamesFromIDs** ignorent le jeu de propriétés et retournent les noms des identificateurs dans le tableau de balises de propriétés. Certaines implémentations retournent des MAPI_E_INVALID_PARAMETER. D’autres implémentations retournent des noms pour les identificateurs de toutes les propriétés du jeu de propriétés. Si le jeu de propriétés PS_PUBLIC_STRINGS, **GetNamesFromIDs** peut renvoyer tous les noms qui ont été créés. Le fait que le fournisseur de services stocke une propriété sous les identificateurs associés aux chaînes publiques est immérial. 
  
Lorsque vous avez terminé avec les noms des propriétés, vérifiez le contenu du paramètre  _lpcPropNames_ pour déterminer si des noms ont été renvoyés. Si c’est le cas, appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer la mémoire pointée par  _lppPropTags_ et  _lpppPropNames_ lorsqu’un résultat réussi est renvoyé. Un appel à **MAPIFreeBuffer est** suffisant pour chaque paramètre ; vous n’avez pas besoin de parcourir le tableau de pointeurs et de libérer chaque structure **MAPINAMEID** individuellement. 
  
Pour plus d’informations sur les propriétés nommées, voir [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedProps  <br/> |MFCMAPI utilise la méthode **IMAPIProp::GetNamesFromIDs** pour rechercher les propriétés nommées qui ont été précédemment mappées.  <br/> |
   
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

