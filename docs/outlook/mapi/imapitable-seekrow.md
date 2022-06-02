---
title: IMAPITableSeekRow
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPITableSeekRow, qui déplace le curseur vers une position spécifique dans la table.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.SeekRow
api_type:
- COM
ms.assetid: 93ac63ae-f254-45e1-a9b1-347d69d2ed9f
ms.openlocfilehash: b6b925b25094b54d7d026b73feaed9d90bca84a2
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827806"
---
# <a name="imapitableseekrow"></a>IMAPITable::SeekRow

**S’applique à** : Outlook 2013 | Outlook 2016
  
Déplace le curseur vers une position spécifique dans la table.
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a>Paramètres

 _bkOrigin_
  
> [in] Signet identifiant la position de départ de l’opération de recherche. Un signet peut être créé à l’aide de la méthode [IMAPITable::CreateBookmark](imapitable-createbookmark.md) , ou l’une des valeurs prédéfinies suivantes peut être passée.

BOOKMARK_BEGINNING
  
> Démarre l’opération de recherche à partir du début de la table.

BOOKMARK_CURRENT
  
> Démarre l’opération de recherche à partir de la ligne de la table où se trouve le curseur.

BOOKMARK_END
  
> Démarre l’opération de recherche à partir de la fin de la table.

 _lRowCount_
  
> [in] Nombre signé du nombre de lignes à déplacer, à partir du signet identifié par le paramètre  _bkOrigin_ .

 _lplRowsSought_
  
> [out] Si  _lRowCount_ est un pointeur valide en entrée, _lplRowsSought_ pointe vers le nombre de lignes qui ont été traitées dans l’opération de recherche, dont le signe indique la direction de la recherche, vers l’avant ou vers l’arrière. Si  _lRowCount_ est négatif,  _lplRowsSought_ est négatif.

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L’opération de recherche a réussi.

MAPI_E_BUSY
  
> Une autre opération est en cours qui empêche le démarrage de l’opération de recherche de lignes. Soit l’opération en cours doit être autorisée à se terminer, soit elle doit être arrêtée.

MAPI_E_INVALID_BOOKMARK
  
> Le signet spécifié dans le paramètre _bkOrigin_ n’est pas valide parce qu’il a été supprimé ou parce qu’il est au-delà de la dernière ligne demandée.

MAPI_W_POSITION_CHANGED
  
> L’appel a réussi, mais le signet spécifié dans le paramètre _bkOrigin_ n’est plus défini sur la même ligne qu’au moment de sa dernière utilisation. Si le signet n’a pas été utilisé, il n’est plus dans la même position que lors de sa création. Lorsque cet avertissement est retourné, l’appel doit être traité comme ayant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).

## <a name="remarks"></a>Remarques

La méthode **IMAPITable::SeekRow** établit une nouvelle position BOOKMARK_CURRENT pour le curseur. Le paramètre  _lRowCount_ indique le nombre de lignes que le curseur déplace et la direction du mouvement.
  
Si la position obtenue se trouve au-delà de la dernière ligne du tableau, le curseur est positionné après la dernière ligne. Si la position obtenue se trouve avant la première ligne de la table, le curseur est positionné au début de la première ligne.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si la ligne pointée par  _bkOrigin_ n’existe plus dans la table et que vous ne pouvez pas établir de nouvelle position pour le signet, retournez MAPI_E_INVALID_BOOKMARK. Si la ligne pointant vers by_bkOrigin_no existe plus longtemps et que vous pouvez établir une nouvelle position pour le signet, retournez MAPI_W_POSITION_CHANGED.
  
Un signet pointant vers une ligne qui est réduite hors de la vue de table peut toujours être utilisé. Si l’appelant tente de déplacer le curseur vers un tel signet, déplacez le curseur vers la ligne visible suivante et retournez MAPI_W_POSITION_CHANGED.
  
Vous pouvez déplacer des signets pour les positions réduites hors vue, soit au moment de l’utilisation, soit au moment où la ligne est réduite. Si un signet est déplacé au moment où la ligne est réduite, conservez un peu dans le signet qui indique si le signet a été déplacé depuis sa dernière utilisation ou, s’il n’a jamais été utilisé, depuis sa création.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour indiquer un déplacement vers l’arrière pour **SeekRow**, passez une valeur négative dans  _lRowCount_. Pour effectuer une recherche au début de la table, passez zéro dans  _lRowCount_ et la valeur BOOKMARK_BEGINNING dans  _bkOrigin_.
  
S’il y a un grand nombre de lignes dans la table, l’opération **SeekRow** peut être lente. Les performances peuvent également être affectées si vous avez besoin d’un nombre de lignes à retourner dans le contenu du paramètre  _lplRowsSought_ .
  
 **SeekRow** retourne le nombre de lignes réellement recherchées, positives ou négatives, dans la variable pointée par  _lRowCount_. Dans une opération ordinaire, elle doit retourner la même valeur pour  _lplRowsSought_ que pour  _lRowCount_, sauf si la recherche a atteint le début ou la fin de la table.
  
Ne définissez pas  _lRowCount_ sur un nombre supérieur à 50. Pour rechercher un plus grand nombre de lignes, utilisez la méthode [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) .
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProcessor.cpp  <br/> |CMAPIProcessor::P rocessMailboxTable  <br/> |MFCMAPI utilise la méthode **IMAPITable::SeekRow** pour localiser le début de la table avant le traitement. |

## <a name="see-also"></a>Voir aussi

[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
