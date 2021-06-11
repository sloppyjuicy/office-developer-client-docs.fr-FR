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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fbc990a8c962883aa07987b200d1d2fd55434f93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413044"
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

## <a name="parameters"></a>Parameters

 _bkOrigin_
  
> [in] Signet identifiant la position de départ de l’opération de recherche. Un signet peut être créé à l’aide de la méthode [IMAPITable::CreateBookmark,](imapitable-createbookmark.md) ou l’une des valeurs prédéfinës suivantes peut être passée. 
    
BOOKMARK_BEGINNING 
  
> Démarre l’opération de recherche à partir du début du tableau. 
    
BOOKMARK_CURRENT 
  
> Démarre l’opération de recherche à partir de la ligne du tableau où se trouve le curseur. 
    
BOOKMARK_END 
  
> Démarre l’opération de recherche à partir de la fin de la table. 
    
 _lRowCount_
  
> [in] Nombre signé du nombre de lignes à déplacer, à partir du signet identifié par le _paramètre bkOrigin._ 
    
 _lplRowsSought_
  
> [out] Si  _lRowCount_ est un pointeur valide sur l’entrée,  _lplRowsSought_ pointe vers le nombre de lignes qui ont été traitées dans l’opération de recherche, dont le signe indique la direction de la recherche, vers l’avant ou vers l’arrière. Si  _lRowCount est_ négatif,  _lplRowsSought_ est négatif. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération de recherche a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche le démarrage de l’opération de recherche de lignes. L’opération en cours doit être autorisée ou arrêtée.
    
MAPI_E_INVALID_BOOKMARK 
  
> Le signet spécifié dans le paramètre  _bkOrigin_ n’est pas valide car il a été supprimé ou parce qu’il se trouve au-delà de la dernière ligne demandée. 
    
MAPI_W_POSITION_CHANGED 
  
> L’appel a réussi, mais le signet spécifié dans le paramètre  _bkOrigin_ n’est plus définie sur la même ligne que lors de sa dernière utilisation. Si le signet n’a pas été utilisé, il n’est plus à la même position qu’au moment de sa création. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED.** Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Remarques

La **méthode IMAPITable::SeekRow** établit une nouvelle position BOOKMARK_CURRENT position du curseur. Le  _paramètre lRowCount_ indique le nombre de lignes que le curseur déplace et la direction du mouvement. 
  
Si la position résultante se trouve au-delà de la dernière ligne du tableau, le curseur est placé après la dernière ligne. Si la position résultante se trouve avant la première ligne du tableau, le curseur est placé au début de la première ligne. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si la ligne pointée par  _bkOrigin_ n’existe plus dans le tableau et que vous ne pouvez pas établir une nouvelle position pour le signet, renvoyez MAPI_E_INVALID_BOOKMARK. Si la ligne pointée par  _bkOrigin_ n’existe plus et que vous pouvez établir une nouvelle position pour le signet, renvoyez MAPI_W_POSITION_CHANGED. 
  
Un signet pointant vers une ligne qui est réduire en dehors de l’affichage Tableau peut toujours être utilisé. Si l’appelant tente de déplacer le curseur vers un signet de ce type, déplacez le curseur vers la ligne visible suivante et renvoyez-MAPI_W_POSITION_CHANGED. 
  
Vous pouvez déplacer des signets pour les positions qui sont en dehors de l’affichage, soit au moment de l’utilisation, soit au moment où la ligne est réduire. Si un signet est déplacé au moment où la ligne est réduire, conservez un peu dans le signet qui indique si le signet a été déplacé depuis sa dernière utilisation ou, s’il n’a jamais été utilisé, depuis sa création.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour indiquer un déplacement vers l’arrière **pour SeekRow**, passez une valeur négative dans  _lRowCount_. Pour rechercher au début du tableau, passez zéro dans  _lRowCount_ et la valeur BOOKMARK_BEGINNING dans  _bkOrigin_. 
  
S’il y a beaucoup de lignes dans le tableau, **l’opération SeekRow** peut être lente. Les performances peuvent également être affectées si vous avez besoin de retourner un nombre de lignes dans le contenu du _paramètre lplRowsSought._ 
  
 **SeekRow** renvoie le nombre de lignes réellement recherchés dans, positif ou négatif, dans la variable pointée par  _lRowCount_. En opération ordinaire, elle doit renvoyer la même valeur pour  _lplRowsSought_ que pour  _lRowCount_, sauf si la recherche a atteint le début ou la fin du tableau. 
  
Ne définissez  _pas lRowCount_ sur un nombre supérieur à 50. Pour rechercher un plus grand nombre de lignes, utilisez la méthode [IMAPITable::SeekRowApprox.](imapitable-seekrowapprox.md) 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProcessor.cpp  <br/> |CMAPIProcessor::P rocessMailboxTable  <br/> |MFCMAPI utilise la **méthode IMAPITable::SeekRow** pour localiser le début de la table avant le traitement.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

