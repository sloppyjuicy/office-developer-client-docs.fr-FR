---
title: IMAPITableFindRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FindRow
api_type:
- COM
ms.assetid: 6511368c-9777-497e-9eea-cf390c04b92e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a5364af229721d101f38d2f054f528169b48c09e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329078"
---
# <a name="imapitablefindrow"></a>IMAPITable::FindRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche la ligne suivante d'une table qui correspond aux critères de recherche spécifiques et place le curseur sur cette ligne.
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpRestriction_
  
> dans Pointeur vers une structure [SRestriction](srestriction.md) qui décrit les critères de recherche. 
    
 _BkOrigin_
  
> dans Signet identifiant la ligne où **FindRow** doit commencer sa recherche. Un signet peut être créé à l'aide de la méthode [IMAPITable:: CreateBookmark](imapitable-createbookmark.md) ou l'une des valeurs prédéfinies suivantes peut être passée. 
    
BOOKMARK_BEGINNING 
  
> Recherche à partir du début de la table. 
    
BOOKMARK_CURRENT 
  
> Recherche à partir de la ligne dans la table où se trouve le curseur. 
    
BOOKMARK_END 
  
> Recherches à partir de la fin du tableau. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la direction de la recherche. L'indicateur suivant peut être défini:
    
DIR_BACKWARD 
  
> Effectue une recherche vers l'arrière à partir de la ligne identifiée par le signet.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'opération de recherche a réussi.
    
MAPI_E_INVALID_BOOKMARK 
  
> Le signet dans le paramètre _BkOrigin_ n'est pas valide, car il a été supprimé ou il se trouve au-delà de la dernière ligne demandée. 
    
MAPI_E_NOT_FOUND 
  
> Aucune ligne correspondant à la restriction n'a été trouvée.
    
MAPI_W_POSITION_CHANGED
  
> L'appel a réussi, mais le signet utilisé dans l'opération n'est plus défini sur la même ligne que lors de sa dernière utilisation; Si le signet n'a pas été utilisé, il n'est plus dans la même position que lors de sa création. Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable:: FindRow** localise la première ligne de la table pour qu'elle corresponde à un ensemble de critères de recherche décrits dans la structure **SRestriction** vers laquelle pointe le paramètre _lpRestriction_ . 
  
En règle générale, **FindRow** effectue une recherche vers l'avant à partir du signet spécifié. L'appelant peut définir la recherche pour reculer à partir du signet en définissant l'indicateur DIR_BACKWARD dans le paramètre _ulFlags_ . La recherche vers le bas commence à partir du signet actif; la recherche vers l'arrière commence à partir de la ligne précédant le signet. La position de fin de la recherche est juste avant la première ligne ayant satisfait à la restriction. 
  
Si la ligne désignée par le signet dans le paramètre _BkOrigin_ n'existe plus dans le tableau et que la table ne peut pas établir de nouvelle position pour le signet, **FindRow** renvoie MAPI_E_INVALID_BOOKMARK. Si la ligne sur laquelle pointe _BkOrigin_ n'existe plus et que la table est en mesure d'établir une nouvelle position pour le signet, **FindRow** renvoie MAPI_W_POSITION_CHANGED. 
  
Si le signet transmis dans _BkOrigin_ est BOOKMARK_BEGINNING ou BOOKMARK_END, **FindRow** renvoie MAPI_E_NOT_FOUND si aucune ligne correspondante n'est trouvée. Si le signet utilisé dans _BkOrigin_ est BOOKMARK_CURRENT, **FINDROW** peut renvoyer MAPI_W_POSITION_CHANGED mais pas MAPI_E_INVALID_BOOKMARK, car il y a toujours une position de curseur actuelle. 
  
La colonne de propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) est requise pour toutes les tables et toutes les implémentations de **FindRow** doivent prendre en charge les appels qui recherchent une ligne en fonction de PR_INSTANCE_KEY. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Le type de recherche de préfixe effectué par **FindRow** n'est utile que si la recherche respecte la même direction que l'organisation de la table. Pour obtenir le comportement requis, la fonction de comparaison impliquée par le **RELOP_GE** passé dans la structure de restriction de propriété doit être la même fonction de comparaison que l'ordre de tri de la table. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser **FindRow** pour prendre en charge le défilement basé sur les chaînes tapées par l'utilisateur, en particulier dans les zones de liste dans les boîtes de dialogue d'adresses. Dans ce type de défilement, les utilisateurs entrent des préfixes progressivement plus longs d'une valeur de chaîne souhaitée et vous pouvez périodiquement émettre un appel **FindRow** pour accéder à la première ligne correspondant au préfixe. La direction du curseur dépend de la direction dans laquelle la recherche est exécutée. 
  
Pour utiliser **FindRow**, un signet doit être défini. La recherche de chaîne peut provenir de n'importe quel signet, y compris des signets prédéfinis indiquant la position actuelle et le début et la fin du tableau. S'il existe un grand nombre de lignes dans la table, l'opération de recherche peut être lente.
  
Utilisez une restriction pour rechercher un préfixe de chaîne pour le défilement, comme suit. Pour effectuer une recherche vers l'avant sur une colonne triée par ordre croissant et pour effectuer une recherche vers l'arrière sur une colonne triée dans l'ordre décroissant, transmettez une structure de restriction de propriété dans le paramètre _lpRestriction_ avec la relation **RELOP_GE** et l'objet balise et préfixe de propriété à l'aide du préfixe de _balise_ **GE** __. 
  
Pour plus d'informations sur l'utilisation des structures de restriction pour spécifier un filtre, consultez la rubrique [à propos des restrictions](about-restrictions.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI utilise la méthode **IMAPITable:: FindRow** pour rechercher les lignes correspondant à une restriction.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

