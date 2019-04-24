---
title: IMAPITableSeekRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRow
api_type:
- COM
ms.assetid: 93ac63ae-f254-45e1-a9b1-347d69d2ed9f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fbc990a8c962883aa07987b200d1d2fd55434f93
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328825"
---
# <a name="imapitableseekrow"></a>IMAPITable::SeekRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Déplace le curseur à une position spécifique dans le tableau.
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a>Paramètres

 _bkOrigin_
  
> dans Signet identifiant la position de départ de l'opération de recherche. Un signet peut être créé à l'aide de la méthode [IMAPITable:: CreateBookmark](imapitable-createbookmark.md) ou l'une des valeurs prédéfinies suivantes peut être passée. 
    
BOOKMARK_BEGINNING 
  
> Démarre l'opération Seek à partir du début de la table. 
    
BOOKMARK_CURRENT 
  
> Démarre l'opération Seek à partir de la ligne dans la table où se trouve le curseur. 
    
BOOKMARK_END 
  
> Démarre l'opération Seek à partir de la fin de la table. 
    
 _lRowCount_
  
> dans Nombre signé du nombre de lignes à déplacer, en commençant par le signet identifié par le paramètre _bkOrigin_ . 
    
 _lplRowsSought_
  
> remarquer Si _lRowCount_ est un pointeur valide sur l'entrée, _lplRowsSought_ pointe vers le nombre de lignes traitées dans l'opération Seek, dont le signe indique le sens de la recherche, à l'avant ou vers l'arrière. Si _lRowCount_ est négatif, _lplRowsSought_ est négatif. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'opération Seek a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours, ce qui empêche le démarrage de l'opération de recherche de lignes. L'opération en cours doit être autorisée ou elle doit être arrêtée.
    
MAPI_E_INVALID_BOOKMARK 
  
> Le signet spécifié dans le paramètre _bkOrigin_ n'est pas valide car il a été supprimé ou parce qu'il se trouve au-delà de la dernière ligne demandée. 
    
MAPI_W_POSITION_CHANGED 
  
> L'appel a réussi, mais le signet spécifié dans le paramètre _bkOrigin_ n'est plus défini sur la même ligne que lors de sa dernière utilisation. Si le signet n'a pas été utilisé, il n'est plus dans la même position qu'il l'était lors de sa création. Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable:: SeekRow** établit une nouvelle position BOOKMARK_CURRENT pour le curseur. Le paramètre _lRowCount_ indique le nombre de lignes que le curseur déplace et le sens du mouvement. 
  
Si la position résultante se trouve au-delà de la dernière ligne du tableau, le curseur est positionné après la dernière ligne. Si la position obtenue se trouve avant la première ligne de la table, le curseur est positionné au début de la première ligne. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si la ligne sur laquelle pointe _bkOrigin_ n'existe plus dans le tableau et que vous ne pouvez pas établir une nouvelle position pour le signet, renvoyez MAPI_E_INVALID_BOOKMARK. Si la ligne sur laquelle pointe _bkOrigin_ n'existe plus et que vous pouvez établir une nouvelle position pour le signet, renvoyez MAPI_W_POSITION_CHANGED. 
  
Un signet pointant vers une ligne qui est réduite de la vue tableau peut toujours être utilisé. Si l'appelant tente de déplacer le curseur vers un signet de ce type, déplacez le curseur sur la ligne visible suivante et renvoyez MAPI_W_POSITION_CHANGED. 
  
Vous pouvez déplacer les signets des positions réduites en vue, soit au moment de l'utilisation, soit au moment de la réduction de la ligne. Si un signet est déplacé au moment où la ligne est réduite, conservez un bit qui indique si le signet a été déplacé depuis sa dernière utilisation ou, s'il n'a jamais été utilisé, depuis sa création.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour indiquer un déplacement vers l'arrière pour la propriété **SeekRow**, transmettez une valeur négative dans _lRowCount_. Pour effectuer une recherche jusqu'au début de la table, transmettez zéro dans _lRowCount_ et la valeur BOOKMARK_BEGINNING dans _bkOrigin_. 
  
S'il y a beaucoup de lignes dans la table, l'opération **SeekRow** peut être lente. Les performances peuvent également être affectées si vous avez besoin d'un nombre de lignes à renvoyer dans le contenu du paramètre _lplRowsSought_ . 
  
 **SeekRow** renvoie le nombre de lignes réellement recherchées, positives ou négatives, dans la variable désignée par _lRowCount_. En fonctionnement normal, elle doit renvoyer la même valeur pour _lplRowsSought_ que celle qui a été transmise pour _lRowCount_, sauf si la recherche a atteint le début ou la fin de la table. 
  
N'affectez pas un nombre supérieur à 50 à _lRowCount_ . Pour rechercher un plus grand nombre de lignes, utilisez la méthode [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProcessor. cpp  <br/> |CMAPIProcessor::P rocessMailboxTable  <br/> |MFCMAPI utilise la méthode **IMAPITable:: SeekRow** pour localiser le début de la table avant le traitement.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

