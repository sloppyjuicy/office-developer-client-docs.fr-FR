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
ms.openlocfilehash: cb777074d1657a3ee5c2f1e9f70d2b304858c1b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784078"
---
# <a name="imapitablefindrow"></a>IMAPITable::FindRow

  
  
**S’applique à**: Outlook 
  
Trouve la ligne suivante dans une table qui correspond aux critères de recherche spécifiques et place le curseur sur cette ligne.
  
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
  
> [in] Un signet qui identifie la ligne où **FindRow** doit commencer la recherche. Un signet peut être créé à l’aide de la méthode [IMAPITable::CreateBookmark](imapitable-createbookmark.md) ou une des valeurs prédéfinies suivantes peut être passée. 
    
BOOKMARK_BEGINNING 
  
> Recherche à partir du début de la table. 
    
BOOKMARK_CURRENT 
  
> Recherche à partir de la ligne dans le tableau où se trouve le curseur. 
    
BOOKMARK_END 
  
> Recherche de la fin de la table. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la direction de la recherche. Vous pouvez définir l’indicateur suivant :
    
DIR_BACKWARD 
  
> Recherche en arrière à partir de la ligne identifiée par le signet.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’opération de recherche a réussi.
    
MAPI_E_INVALID_BOOKMARK 
  
> Le signet dans le paramètre _BkOrigin_ n’est pas valide car il a été supprimé ou étant au-delà de la dernière ligne demandée. 
    
MAPI_E_NOT_FOUND 
  
> Aucune ligne n’a été trouvé correspondant à la restriction.
    
MAPI_W_POSITION_CHANGED
  
> L’appel a réussi, mais le signet utilisé dans l’opération n’est plus défini au niveau de la même ligne que lorsqu’il a été utilisé dernière ; Si le signet n’a pas été utilisé, il n’est plus dans la même position que lors de sa création. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Consultez [utilisation de Macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::FindRow** localise la première ligne du tableau à correspondent à un ensemble de critères de recherche décrites dans la structure **SRestriction** désignée par le paramètre _lpRestriction_ . 
  
En règle générale, **FindRow** effectue la recherche vers l’avant le signet spécifié. L’appelant peut affecter à la recherche pour revenir en arrière à partir du signet en définissant l’indicateur DIR_BACKWARD dans le paramètre _ulFlags_ . Transférer la recherche démarre à partir du signet actuel ; la recherche vers l’arrière commence à partir de la ligne avant le signet. La position de fin de la recherche est juste avant la première ligne trouvée qui satisfait la restriction. 
  
Si la ligne sur laquelle pointée le signet dans le paramètre _BkOrigin_ n’existe plus dans la table et la table ne peut pas établir une nouvelle position du signet, **FindRow** renvoie MAPI_E_INVALID_BOOKMARK. Si la ligne désignée par _BkOrigin_ n’existe plus et la table est en mesure d’établir une nouvelle position du signet, **FindRow** renvoie MAPI_W_POSITION_CHANGED. 
  
Si le signet passé _BkOrigin_ est BOOKMARK_BEGINNING ou BOOKMARK_END, **FindRow** renvoie MAPI_E_NOT_FOUND si aucune ligne n’est trouvée. Si le signet utilisé dans _BkOrigin_ est BOOKMARK_CURRENT, **FindRow** peut renvoyer MAPI_W_POSITION_CHANGED mais pas MAPI_E_INVALID_BOOKMARK, car il y a toujours une position actuelle du curseur. 
  
La colonne de la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) est requise pour toutes les tables, et toutes les implémentations de **FindRow** sont nécessaires pour prendre en charge des appels qui recherchent une ligne basée sur PR_INSTANCE_KEY. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Le type de préfixe recherche effectuée par **FindRow** n’est utile lors de la recherche suit le même sens que l’organisation de la table. Pour obtenir le comportement requis, la fonction de comparaison impliquée par le **RELOP_GE** passé dans la structure de restriction de propriété doit être la même fonction de comparaison sur laquelle repose l’ordre de tri du tableau. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez utiliser **FindRow** pour prendre en charge le défilement basées sur les chaînes entrés par l’utilisateur, notamment dans les zones de liste adresse boîtes de dialogue. Dans ce type de défilement, les utilisateurs entrent des préfixes progressivement plus d’une valeur de chaîne souhaitée, et vous pouvez régulièrement émettre un appel **FindRow** pour accéder à la première ligne qui correspond au préfixe. Le sens dans lequel passe le curseur dépend de la direction dans laquelle la recherche est définie sur Exécuter. 
  
Pour utiliser **FindRow**, un signet doit être défini. La recherche de chaîne peut provenir d’un signet, notamment les signets prédéfinis qui indique la position actuelle et le début et la fin de la table. S’il existe un grand nombre de lignes de la table, l’opération de recherche peut être lente.
  
Une restriction permet de rechercher un préfixe de chaîne pour le défilement comme suit. Pour transférer une recherche sur une colonne triée par ordre croissant et pour la recherche vers l’arrière sur une colonne de tri dans l’ordre décroissant, transmettez une structure de restriction de propriété dans le paramètre _lpRestriction_ avec la relation **RELOP_GE** et approprié balise de propriété et le préfixe, à l’aide de la _balise_ de format **GE** _préfixe_. 
  
Pour plus d’informations sur l’utilisation des structures de restriction pour spécifier un filtre, voir [à propos des Restrictions](about-restrictions.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI utilise la méthode **IMAPITable::FindRow** pour rechercher les lignes qui correspondent à une restriction.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

