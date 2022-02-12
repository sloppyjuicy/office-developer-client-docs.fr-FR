---
title: IMAPITableFindRow
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a3df218faf2c34b4f2e056310e6b204fcd407b72
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776416"
---
# <a name="imapitablefindrow"></a>IMAPITable::FindRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche la ligne suivante dans un tableau qui correspond à des critères de recherche spécifiques et déplace le curseur vers cette ligne.
  
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
  
> [in] Signet identifiant la ligne dans laquelle **FindRow** doit commencer sa recherche. Un signet peut être créé à l’aide de la méthode [IMAPITable::CreateBookmark](imapitable-createbookmark.md) , ou l’une des valeurs prédéfinës suivantes peut être passée. 
    
BOOKMARK_BEGINNING 
  
> Recherche depuis le début du tableau. 
    
BOOKMARK_CURRENT 
  
> Recherche à partir de la ligne du tableau où se trouve le curseur. 
    
BOOKMARK_END 
  
> Recherche à partir de la fin du tableau. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la direction de la recherche. L’indicateur suivant peut être définie :
    
DIR_BACKWARD 
  
> Recherche vers l’arrière à partir de la ligne identifiée par le signet.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération de recherche a réussi.
    
MAPI_E_INVALID_BOOKMARK 
  
> Le signet dans le _paramètre BkOrigin_ n’est pas valide car il a été supprimé ou parce qu’il se trouve au-delà de la dernière ligne demandée. 
    
MAPI_E_NOT_FOUND 
  
> Aucune ligne qui correspondait à la restriction n’a été trouvée.
    
MAPI_W_POSITION_CHANGED
  
> L’appel a réussi, mais le signet utilisé dans l’opération n’est plus définie sur la même ligne que lors de sa dernière utilisation . si le signet n’a pas été utilisé, il n’est plus au même endroit que lors de sa création. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED’avertissement** . Voir [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La **méthode IMAPITable::FindRow** localise la première ligne du tableau pour correspondre à un ensemble de critères de recherche décrits dans la structure **SRestriction** pointée par le paramètre  _lpRestriction_ . 
  
En règle générale, **FindRow** recherche vers l’avant à partir du signet spécifié. L’appelant peut définir la recherche pour qu’elle se déplace vers l’arrière à partir du signet en DIR_BACKWARD dans le _paramètre ulFlags_ . La recherche vers l’avant commence à partir du signet actuel ; la recherche vers l’arrière commence à partir de la ligne précédant le signet. La position de fin de la recherche se trouve juste avant la première ligne trouvée qui a satisfait à la restriction. 
  
Si la ligne pointée par le signet dans le paramètre _BkOrigin_ n’existe plus dans le tableau et que la table ne peut pas établir une nouvelle position pour le signet, **FindRow** renvoie MAPI_E_INVALID_BOOKMARK. Si la ligne pointée par  _BkOrigin_ n’existe plus et que le tableau est en mesure d’établir une nouvelle position pour le signet, **FindRow** renvoie MAPI_W_POSITION_CHANGED. 
  
Si le signet transmis dans  _BkOrigin_ est BOOKMARK_BEGINNING ou BOOKMARK_END, **FindRow** renvoie MAPI_E_NOT_FOUND si aucune ligne correspondante n’est trouvée. Si le signet utilisé dans  _BkOrigin_ est BOOKMARK_CURRENT, **FindRow** peut renvoyer MAPI_W_POSITION_CHANGED mais pas MAPI_E_INVALID_BOOKMARK car il existe toujours une position de curseur actuelle. 
  
La **colonne PR_INSTANCE_KEY** propriété ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) est requise pour toutes les tables et toutes les implémentations de **FindRow** sont requises pour prendre en charge les appels recherchant une ligne basée sur PR_INSTANCE_KEY. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Le type de recherche de préfixe effectué par **FindRow** est utile uniquement lorsque la recherche suit la même direction que l’organisation de la table. Pour obtenir le comportement requis, la fonction de comparaison impliquée par le **RELOP_GE** passé dans la structure de restriction de propriété doit être la même fonction de comparaison sur laquelle repose l’ordre de tri du tableau. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser **FindRow** pour prendre en charge le défilement en fonction des chaînes tapées par l’utilisateur, en particulier dans les zones de liste dans les boîtes de dialogue d’adresse. Dans ce type de défilement, les utilisateurs entrent progressivement des préfixes plus longs d’une valeur de chaîne souhaitée et vous pouvez régulièrement émettre un appel **FindRow** pour accéder à la première ligne qui correspond au préfixe. La direction dans laquelle le curseur passe dépend de la direction dans laquelle la recherche est définie pour s’exécuter. 
  
Pour utiliser **FindRow**, vous devez définir un signet. La recherche de chaîne peut provenir de n’importe quel signet, y compris des signets prédéfins indiquant la position actuelle et le début et la fin du tableau. Si le tableau compte un grand nombre de lignes, l’opération de recherche peut être lente.
  
Utilisez une restriction pour rechercher un préfixe de chaîne à faire défiler comme suit. Pour la recherche vers l’avant sur une colonne triée par ordre croissant et pour la recherche vers l’arrière sur une colonne triée dans l’ordre décroit, passez une structure de restriction de propriété dans le paramètre _lpRestriction_ avec la **relation RELOP_GE** et la balise de propriété et le préfixe appropriés, à l’aide du _préfixe_ **GE** de _balise_ de format. 
  
Pour plus d’informations sur l’utilisation de structures de restriction pour spécifier un filtre, voir [À propos des restrictions](about-restrictions.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI utilise la **méthode IMAPITable::FindRow** pour rechercher les lignes qui correspondent à une restriction. |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

