---
title: IMAPITableFindRow
description: IMAPITableFindRow recherche la ligne suivante dans une table qui correspond à des critères de recherche spécifiques et déplace le curseur vers cette ligne.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.FindRow
api_type:
- COM
ms.assetid: 6511368c-9777-497e-9eea-cf390c04b92e
ms.openlocfilehash: 8ed42b9ddbfa5b0de2bf84c8872bd5f3e0ce72ec
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827848"
---
# <a name="imapitablefindrow"></a>IMAPITable::FindRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche la ligne suivante dans une table qui correspond à des critères de recherche spécifiques et déplace le curseur vers cette ligne.
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpRestriction_
  
> [in] Pointeur vers une structure [SRestriction](srestriction.md) qui décrit les critères de recherche. 
    
 _BkOrigin_
  
> [in] Signet identifiant la ligne où **FindRow** doit commencer sa recherche. Un signet peut être créé à l’aide de la méthode [IMAPITable::CreateBookmark](imapitable-createbookmark.md) , ou l’une des valeurs prédéfinies suivantes peut être passée. 
    
BOOKMARK_BEGINNING 
  
> Recherche à partir du début de la table. 
    
BOOKMARK_CURRENT 
  
> Recherche à partir de la ligne de la table où se trouve le curseur. 
    
BOOKMARK_END 
  
> Recherche à partir de la fin de la table. 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la direction de la recherche. L’indicateur suivant peut être défini :
    
DIR_BACKWARD 
  
> Effectue une recherche vers l’arrière à partir de la ligne identifiée par le signet.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération de recherche a réussi.
    
MAPI_E_INVALID_BOOKMARK 
  
> Le signet dans le paramètre _BkOrigin_ n’est pas valide car il a été supprimé ou parce qu’il est au-delà de la dernière ligne demandée. 
    
MAPI_E_NOT_FOUND 
  
> Aucune ligne correspondant à la restriction n’a été trouvée.
    
MAPI_W_POSITION_CHANGED
  
> L’appel a réussi, mais le signet utilisé dans l’opération n’est plus défini sur la même ligne que lors de sa dernière utilisation ; si le signet n’a pas été utilisé, il n’est plus dans la même position que lors de sa création. Lorsque cet avertissement est retourné, l’appel doit être traité comme ayant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::FindRow** localise la première ligne de la table pour qu’elle corresponde à un ensemble de critères de recherche décrits dans la structure **SRestriction** pointée par le paramètre  _lpRestriction_ . 
  
En règle générale, **FindRow** effectue une recherche vers l’avant à partir du signet spécifié. L’appelant peut définir la recherche pour qu’elle se déplace vers l’arrière du signet en définissant l’indicateur DIR_BACKWARD dans le paramètre _ulFlags_ . La recherche en avant commence à partir du signet actuel ; la recherche vers l’arrière commence à partir de la ligne antérieure au signet. La position de fin de la recherche se situe juste avant que la première ligne trouvée ne satisfaise à la restriction. 
  
Si la ligne pointée par le signet dans le paramètre _BkOrigin_ n’existe plus dans la table et que la table ne peut pas établir de nouvelle position pour le signet, **FindRow** retourne MAPI_E_INVALID_BOOKMARK. Si la ligne pointée par  _BkOrigin_ n’existe plus et que la table est en mesure d’établir une nouvelle position pour le signet, **FindRow** retourne MAPI_W_POSITION_CHANGED. 
  
Si le signet passé dans  _BkOrigin_ est BOOKMARK_BEGINNING ou BOOKMARK_END, **FindRow** renvoie MAPI_E_NOT_FOUND si aucune ligne correspondante n’est trouvée. Si le signet utilisé dans  _BkOrigin_ est BOOKMARK_CURRENT, **FindRow** peut retourner MAPI_W_POSITION_CHANGED mais pas MAPI_E_INVALID_BOOKMARK, car il existe toujours une position de curseur actuelle. 
  
La colonne de propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) est requise pour toutes les tables, et toutes les implémentations de **FindRow** sont requises pour prendre en charge les appels à la recherche d’une ligne en fonction de PR_INSTANCE_KEY. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Le type de recherche de préfixe effectuée par **FindRow** n’est utile que lorsque la recherche suit la même direction que l’organisation de la table. Pour obtenir le comportement requis, la fonction de comparaison implicite par **l’RELOP_GE** passée dans la structure de restriction de propriété doit être la même fonction de comparaison sur laquelle l’ordre de tri de table est basé. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser **FindRow** pour prendre en charge le défilement en fonction des chaînes tapées par l’utilisateur, en particulier dans les zones de liste dans les boîtes de dialogue d’adresse. Dans ce type de défilement, les utilisateurs entrent progressivement des préfixes plus longs d’une valeur de chaîne souhaitée, et vous pouvez émettre régulièrement un appel **FindRow** pour accéder à la première ligne qui correspond au préfixe. La direction dans laquelle le curseur saute dépend de la direction à laquelle la recherche est définie pour s’exécuter. 
  
Pour utiliser **FindRow**, un signet doit être défini. La recherche de chaîne peut provenir de n’importe quel signet, y compris des signets prédéfinis indiquant la position actuelle et le début et la fin de la table. S’il existe un grand nombre de lignes dans la table, l’opération de recherche peut être lente.
  
Utilisez une restriction pour rechercher un préfixe de chaîne pour le défilement comme suit. Pour la recherche vers l’avant sur une colonne triée dans l’ordre croissant et pour la recherche descendante sur une colonne triée dans l’ordre décroissant, passez une structure de restriction de propriété dans le paramètre _lpRestriction_ avec le **RELOP_GE** relation et la balise de propriété et le préfixe appropriés, à l’aide du _préfixe_ **GE** _de balise_ de format. 
  
Pour plus d’informations sur l’utilisation de structures de restriction pour spécifier un filtre, consultez [À propos des restrictions](about-restrictions.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI utilise la méthode **IMAPITable::FindRow** pour rechercher les lignes qui correspondent à une restriction. |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

