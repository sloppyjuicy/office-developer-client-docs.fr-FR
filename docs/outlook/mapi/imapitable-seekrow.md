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
ms.openlocfilehash: aead09eb10a3015a54867f14011c56b686bc8624
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586479"
---
# <a name="imapitableseekrow"></a>IMAPITable::SeekRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Déplace le curseur à un emplacement spécifique dans le tableau.
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a>Paramètres

 _bkOrigin_
  
> [in] Signet qui identifie la position de départ pour l’opération de recherche. Un signet peut être créé à l’aide de la méthode [IMAPITable::CreateBookmark](imapitable-createbookmark.md) ou une des valeurs prédéfinies suivantes peut être passée. 
    
BOOKMARK_BEGINNING 
  
> Démarre l’opération de recherche à partir du début de la table. 
    
BOOKMARK_CURRENT 
  
> Démarre l’opération de recherche à partir de la ligne dans le tableau où se trouve le curseur. 
    
BOOKMARK_END 
  
> Démarre l’opération de recherche à partir de la fin de la table. 
    
 _lRowCount_
  
> [in] Décompte signé du nombre de lignes à déplacer, à partir du signet identifié par le paramètre _bkOrigin_ . 
    
 _lplRowsSought_
  
> [out] Si _lRowCount_ est un pointeur valid sur les points d’entrée, _lplRowsSought_ au nombre de lignes qui ont été traités dans l’opération de recherche, dont le signe indique la direction de la recherche, avancer ou reculer. Si _lRowCount_ est négatif, _lplRowsSought_ est négatif. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération de recherche a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche l’opération de recherche à la ligne de démarrage. L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.
    
MAPI_E_INVALID_BOOKMARK 
  
> Le signet spécifié dans le paramètre _bkOrigin_ n’est pas valide car il a été supprimé ou étant au-delà de la dernière ligne demandée. 
    
MAPI_W_POSITION_CHANGED 
  
> L’appel a réussi, mais le signet spécifié dans le paramètre _bkOrigin_ n’est plus défini au niveau de la même ligne que lors de la dernière utilisation. Si le signet n’a pas été utilisé, il n’est plus dans la même position telle qu’elle était lors de sa création. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::SeekRow** établit une nouvelle position BOOKMARK_CURRENT pour le curseur. Le paramètre _lRowCount_ indique le nombre de lignes qui déplace le curseur et la direction du déplacement. 
  
Si la position qui en résulte est au-delà de la dernière ligne du tableau, le curseur est positionné après la dernière ligne. Si la position qui en résulte est avant la première ligne du tableau, le curseur est positionné au début de la première ligne. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Si la ligne désignée par _bkOrigin_ n’existe plus dans la table et ne peut pas établir une nouvelle position du signet, retourne MAPI_E_INVALID_BOOKMARK. Si la ligne désignée par _bkOrigin_ n’existe plus et que vous pouvez définir une nouvelle position du signet, renvoyer MAPI_W_POSITION_CHANGED. 
  
Un signet sur une ligne qui est réduite hors de l’affichage tableau peut toujours être utilisé. Si l’appelant essaie de déplacer le curseur vers tel qu’un signet, déplacez le curseur sur la ligne suivante visible et MAPI_W_POSITION_CHANGED. 
  
Vous pouvez déplacer des signets pour les postes réduits en dehors de l’affichage, au moment de l’utilisation ou au moment de la ligne est réduite. Si un signet est déplacé au moment de la ligne est réduite, conservez un peu du signet qui indique si le signet est déplacé par rapport à sa dernière utilisation ou, si elle n’a jamais été utilisé depuis sa création.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour indiquer un déplacement vers l’arrière pour **SeekRow**, transmettez une valeur négative dans _lRowCount_. Pour rechercher au début de la table, passez zéro dans _lRowCount_ et la valeur BOOKMARK_BEGINNING dans _bkOrigin_. 
  
Si un grand nombre de lignes dans le tableau, l’opération **SeekRow** peut être lente. Performances peuvent également être affectées si vous avez besoin d’un nombre de lignes à renvoyer dans le contenu du paramètre _lplRowsSought_ . 
  
 **SeekRow** renvoie le nombre de lignes réellement recherchée par le biais de, positif ou négatif, dans la variable désignée par _lRowCount_. En fonctionnement normal, il doit renvoyer la même valeur pour _lplRowsSought_ comme passé pour _lRowCount_, sauf si la recherche a atteint le début ou la fin de la table. 
  
Ne définissez pas _lRowCount_ à un nombre supérieur à 50. Pour un plus grand nombre de lignes par le biais de recherche, utilisez la méthode [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProcessor.cpp  <br/> |CMAPIProcessor::ProcessMailboxTable  <br/> |MFCMAPI utilise la méthode **IMAPITable::SeekRow** pour localiser le début de la table avant le traitement.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

