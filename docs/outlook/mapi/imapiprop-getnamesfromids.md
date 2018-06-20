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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a2ec6def319b1f4686a61e9f97a936bfeba0d410
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783908"
---
# <a name="imapipropgetnamesfromids"></a>IMAPIProp::GetNamesFromIDs

  
  
**S’applique à**: Outlook 
  
Fournit les noms des propriétés qui correspondent à un ou plusieurs identificateurs de propriété.
  
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
  
> [entrée, sortie] À l’entrée, un pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété ; dans le cas contraire, la valeur NULL, indiquant que tous les noms doivent être retournées. Le membre **cValues** pour le tableau de balise de propriété ne peut pas être 0. Si _lppPropTags_ est un pointeur valid en entrée, **GetNamesFromIDs** renvoie les noms pour chaque identificateur de la propriété incluse dans le tableau. 
    
 _lpPropSetGuid_
  
> [in] Un pointeur vers un GUID ou le [GUID](guid.md) structure, qui identifie un jeu de propriétés. Le paramètre _lpPropSetGuid_ peut pointer vers un jeu de propriétés valide ou peut être NULL. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique le type de noms à renvoyer. Les indicateurs suivants peuvent être utilisés (si les deux indicateurs sont définis, aucun nom n’est retournées) :
    
MAPI_NO_IDS 
  
> Demandes de renvoyer uniquement les noms stockés en tant que chaînes Unicode. 
    
MAPI_NO_STRINGS 
  
> Demandes de renvoyer uniquement les noms enregistrés comme des identificateurs numériques. 
    
 _lpcPropNames_
  
> [out] Un pointeur vers un décompte des pointeurs de nom de propriété dans le tableau indiqué par le paramètre _lppPropNames_ . 
    
 _lpppPropNames_
  
> [out] Pointeur vers un tableau de pointeurs vers des structures [MAPINAMEID](mapinameid.md) qui contient les noms de propriété. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Les noms de propriété ont été renvoyées avec succès. 
    
MAPI_E_NO_SUPPORT 
  
> L’objet ne gère pas les propriétés nommées. 
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais les noms pour une ou plusieurs propriétés n’a pas peuvent être retournés. Les balises de propriété pour les propriétés défectueux ont un type de propriété de **PT_ERROR**. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md). 
    
MAPI_E_INVALID_PARAMETER 
  
> Membre d’une ou plusieurs des entrées du tableau de la propriété tag désignés par _lppPropTags_ **cValues** est défini sur 0. 
    
## <a name="remarks"></a>Remarques

Accès à la plupart des propriétés est par identificateur de la propriété, certaines propriétés accessibles par un nom. La méthode **IMAPIProp::GetNamesFromIDs** peut être appelée pour effectuer les opérations suivantes : 
  
- Récupérer les noms des identificateurs de propriété spécifique dans un jeu de propriétés spécifique.
    
- Récupérer les noms des identificateurs de propriété spécifique dans n’importe quel jeu de propriétés.
    
- Récupérer les noms de toutes les propriétés nommées qui sont incluses dans le mappage de l’objet.
    
Si la valeur _lppPropTags_ points dans un tableau de balise de propriété valide avec un ou plusieurs identificateurs de propriété et _lpPropSetGuid_ sur une propriété valide, **GetNamesFromIDs** ignore le jeu de propriétés et les types de propriétés et renvoie tous les noms qui correspondent aux identificateurs spécifiés. 
  
Si _lppPropTags_ pointe vers un tableau de balise de propriété valide avec un ou plusieurs identificateurs de propriété et _lpPropSetGuid_ est NULL, **GetNamesFromIDs** renvoie tous les noms qui correspondent aux identificateurs spécifiés. 
  
Si un identificateur spécifié ne dispose pas d’un nom, **GetNamesFromIDs** renvoie la valeur NULL en place de cet identificateur dans la structure retournée dans _lpppPropNames_ et retourne également MAPI_W_ERRORS_RETURNED. 
  
Si _lpPropSetGuid_ et _lppPropTags_ sont NULL, **GetNamesFromIDs** alloue un nouveau tableau de balise de propriété et retourne tous les noms de toutes les propriétés de l’objet nommées. 
  
Lorsqu’il n’y a aucun nom à renvoyer, par exemple, car il n’existe aucune propriété dans le jeu de propriétés demandé ou toutes les propriétés sont de type exclu par le paramètre flags, **GetNamesFromIDs** effectue les opérations suivantes : 
  
- Renvoie S_OK.
    
- Affecte une nouvelle structure **SPropTagArray** , définissant le membre **cValues** sur 0. 
    
- Définit le contenu de _lpcPropNames_ à 0. 
    
- Définit le contenu de _lpppPropNames_ sur NULL. 
    
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Si _lpPropSetGuid_ points à un jeu de propriétés valide et un _lppPropTags_ est NULL, le résultat est indéfini. Vous pouvez utiliser une des stratégies suivantes : 
  
- Ignorer le jeu de propriétés et renvoyer les noms pour les identificateurs de tableau de la propriété tag.
    
- Renvoyer les noms pour seulement les identificateurs de tableau de la propriété tag qui appartiennent au jeu de propriétés spécifié.
    
- Échec de l’appel, renvoi MAPI_E_INVALID_PARAMETER. 
    
## <a name="notes-to-callers"></a>Notes aux appelants

Pour récupérer toutes les propriétés d’un objet nommées, vous devez d’abord appeler la méthode l’objet [IMAPIProp::GetPropList](imapiprop-getproplist.md) et puis passer les identificateurs au-dessus de la plage 0 x 8000 à **GetNamesFromIDs**renvoyées.
  
Si vous passez d’un jeu de propriétés valide, mais pas un tableau de balise de propriété valide, être préparé pour des résultats imprévisibles. Certaines implémentations de **GetNamesFromIDs** ignorer le jeu de propriétés et renvoyer les noms pour les identificateurs de tableau de la propriété tag. Certaines implémentations retourner MAPI_E_INVALID_PARAMETER. Toujours implémentations renvoient des noms pour les identificateurs de toutes les propriétés dans le jeu de propriétés. Si le jeu de propriétés est PS_PUBLIC_STRINGS, **GetNamesFromIDs** peut renvoyer tous les noms qui ont été créées jamais. Si le fournisseur de services stocke une propriété sous les identificateurs de chaînes publics est indifférent. 
  
Lorsque vous avez terminé avec les noms de propriété, vérifiez le contenu du paramètre _lpcPropNames_ pour déterminer si des noms ont été retournés. Dans ce cas, appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de la mémoire vers lequel pointée _lppPropTags_ et _lpppPropNames_ lorsqu’un résultat réussi est retourné. Un appel à **MAPIFreeBuffer** est suffisant pour chaque paramètre ; Il est inutile de parcourir le tableau des pointeurs et de libérer chaque structure **MAPINAMEID** individuellement. 
  
Pour plus d’informations sur les propriétés nommées, voir [Les propriétés MAPI nommée](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedProps  <br/> |MFCMAPI utilise la méthode **IMAPIProp::GetNamesFromIDs** pour rechercher des propriétés nommées qui ont déjà été mappées.  <br/> |
   
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
  
[Utilisation de Macros pour la gestion des erreurs](using-macros-for-error-handling.md)

