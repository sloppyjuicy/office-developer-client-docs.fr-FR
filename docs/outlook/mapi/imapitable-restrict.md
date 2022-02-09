---
title: IMAPITableRestrict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.Restrict
api_type:
- COM
ms.assetid: a5bfc190-b58f-44c3-893c-8727df14ee58
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 288c0b126693846ff27e32901a8c8b3660686adf
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62461826"
---
# <a name="imapitablerestrict"></a>IMAPITable::Restrict

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Applique un filtre à un tableau, en réduisant le jeu de lignes uniquement aux lignes correspondant aux critères spécifiés.
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpRestriction_
  
> [in] Pointeur vers une structure [SRestriction](srestriction.md) définissant les conditions du filtre. La transmission de null dans _le paramètre lpRestriction_ supprime le filtre actuel. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le minutage de l’opération de restriction. Les indicateurs suivants peuvent être définies :
    
TBL_ASYNC 
  
> Démarre l’opération de manière asynchrone et renvoie avant la fin de l’opération.
    
TBL_BATCH 
  
> Reporte l’évaluation du filtre jusqu’à ce que les données de la table soient requises.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le filtre a été appliqué avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche le démarrage de l’opération de restriction. L’opération en cours doit être autorisée ou arrêtée.
    
MAPI_E_TOO_COMPLEX 
  
> La table ne peut pas effectuer l’opération, car le filtre spécifique pointé par  _le paramètre lpRestriction_ est trop compliqué. 
    
## <a name="remarks"></a>Remarques

La **méthode IMAPITable::Restrict** établit une restriction ou un filtre sur une table. S’il existe une restriction précédente, elle est ignorée et la nouvelle est appliquée. L’application d’une restriction n’a aucune incidence sur les données sous-jacentes d’une table . Il modifie simplement l’affichage en limitant les lignes qui peuvent être récupérées aux lignes contenant des données qui répondent à la restriction. 
  
Il existe plusieurs types de restrictions, chacune étant décrite avec une structure différente. La structure [SRestriction](srestriction.md) contient deux membres : une valeur qui indique le type de restriction et la structure spécifique applicable à ce type. 
  
Les notifications pour les lignes de tableau masquées par les appels à **Restreindre** ne sont jamais générées. 
  
Une restriction de propriété sur une propriété à valeurs multiples fonctionne comme une restriction sur une propriété à valeur unique. Une propriété à valeurs multiples à utiliser dans une restriction de propriété doit avoir l’indicateur MVI_FLAG définie. S’il n’a pas cet indicateur, il est traité comme un tuple totalement ordonné. Une comparaison de deux colonnes à valeurs multiples compare les éléments de colonne dans l’ordre, en signalant la relation des colonnes à la première indiquité. L’égalité est renvoyée uniquement si les colonnes comparées contiennent les mêmes valeurs dans le même ordre. Si une colonne a moins de valeurs que l’autre, la relation signalée est celle d’une valeur null par rapport à l’autre valeur.
  
Pour plus d’informations sur les restrictions, voir [À propos des restrictions](about-restrictions.md).
  
> [!NOTE]
> Si vous créez des requêtes dynamiques pour rechercher des données sur le serveur, utilisez la méthode **FindRow** au lieu d’utiliser les méthodes **Restrict** et **QueryRows** ensemble. La **méthode Restrict** crée une vue mise en cache qui est utilisée pour évaluer tous les messages ajoutés ou modifiés dans le dossier de base. Si une application cliente utilise **la méthode Restrict** pour chaque requête dynamique, une vue mise en cache est créée pour chaque requête. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour ignorer la restriction actuelle sans en créer une, passez NULL dans  _lpRestriction_.
  
Si un autre appel de table asynchrone est en cours,  ce qui a pour effet de restreindre le retour de MAPI_E_BUSY, vous pouvez appeler [IMAPITable::Abort](imapitable-abort.md) pour arrêter l’appel. 
  
 **La** restriction fonctionne de manière synchrone, sauf si vous définissez l’un des indicateurs. Si vous définissez l’TBL_BATCH, **Restrict** reporte l’évaluation de la restriction, sauf si vous demandez les données. Si l TBL_ASYNC est définie, Restrictoperates de manière asynchrone, ce qui peut renvoyer le résultat avant la fin de l’opération.
  
Tous les signets d’une table sont ignorés lorsqu’un appel à Restreindre est effectué et BOOKMARK_CURRENT, la position actuelle du curseur, est définie au début du tableau. 
  
Si vous tentez d’imposer une restriction de propriété à une propriété qui ne se trouve pas dans le jeu de colonnes du tableau, les résultats ne sont pas définies. Chaque fois que vous ne savez pas si une propriété est prise en charge dans une table, combinez la restriction de propriété avec une restriction qui existe. La restriction existe vérifie l’existence de la propriété avant d’essayer d’imposer la restriction de propriété. 
  
Ne vous attendez pas à recevoir une notification de tableau sur une ligne qui a été filtrée à partir d’une table en raison d’une restriction.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::ApplyRestriction  <br/> |MFCMAPI utilise la **méthode IMAPITable::Restrict** pour définir une restriction sur une table.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

