---
title: IMAPITableRestrict
description: IMAPITableRestrict applique un filtre à une table, ce qui réduit l’ensemble de lignes aux seules lignes correspondant aux critères spécifiés.
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
ms.openlocfilehash: 28b83c26a6d685fb71930bce06d186523bd249f9
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827813"
---
# <a name="imapitablerestrict"></a>IMAPITable::Restrict

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Applique un filtre à une table, ce qui réduit l’ensemble de lignes aux seules lignes correspondant aux critères spécifiés.
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpRestriction_
  
> [in] Pointeur vers une structure [SRestriction](srestriction.md) définissant les conditions du filtre. Le passage de NULL dans le paramètre _lpRestriction_ supprime le filtre actuel. 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôlent le minutage de l’opération de restriction. Les indicateurs suivants peuvent être définis :
    
TBL_ASYNC 
  
> Démarre l’opération de façon asynchrone et retourne avant la fin de l’opération.
    
TBL_BATCH 
  
> Reporte l’évaluation du filtre jusqu’à ce que les données de la table soient requises.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le filtre a été appliqué avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche le démarrage de l’opération de restriction. Soit l’opération en cours doit être autorisée à se terminer, soit elle doit être arrêtée.
    
MAPI_E_TOO_COMPLEX 
  
> La table ne peut pas effectuer l’opération, car le filtre particulier pointé par le paramètre  _lpRestriction_ est trop compliqué. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::Restrict** établit une restriction ou un filtre sur une table. S’il existe une restriction précédente, elle est ignorée et la nouvelle est appliquée. L’application d’une restriction n’a aucune incidence sur les données sous-jacentes d’une table ; il modifie simplement la vue en limitant les lignes pouvant être récupérées aux lignes contenant des données qui satisfont à la restriction. 
  
Il existe plusieurs types de restrictions différents, chacun décrit avec une structure différente. La structure [SRestriction](srestriction.md) contient deux membres : une valeur qui indique le type de restriction et la structure spécifique applicable à ce type. 
  
Les notifications pour les lignes de table masquées par les appels à **Restreindre** ne sont jamais générées. 
  
Une restriction de propriété sur une propriété à valeurs multiples fonctionne comme une restriction sur une propriété à valeur unique. L’indicateur MVI_FLAG doit être défini sur une propriété à valeurs multiples à utiliser dans une restriction de propriété. Si cet indicateur n’est pas défini, il est traité comme un tuple totalement ordonné. Une comparaison de deux colonnes à plusieurs valeurs compare les éléments de colonne dans l’ordre, en signalant la relation des colonnes à la première inégalité. L’égalité est retournée uniquement si les colonnes comparées contiennent les mêmes valeurs dans le même ordre. Si une colonne a moins de valeurs que l’autre, la relation signalée est celle d’une valeur null à l’autre valeur.
  
Pour plus d’informations sur les restrictions, consultez [À propos des restrictions](about-restrictions.md).
  
> [!NOTE]
> Si vous créez des requêtes dynamiques pour rechercher des données sur le serveur, utilisez la méthode **FindRow** au lieu d’utiliser la méthode **Restrict** et la méthode **QueryRows** ensemble. La méthode **Restrict** crée une vue mise en cache qui est utilisée pour évaluer tous les messages ajoutés ou modifiés dans le dossier de base. Si une application cliente utilise la méthode **Restrict** pour chaque requête dynamique, une vue mise en cache est créée pour chaque requête. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour ignorer la restriction actuelle sans en créer une, transmettez NULL dans  _lpRestriction_.
  
Si un autre appel de table asynchrone est en cours, ce qui entraîne le retour de **Restrict** MAPI_E_BUSY, vous pouvez appeler [IMAPITable::Abort](imapitable-abort.md) pour arrêter l’appel. 
  
 **Restrict** fonctionne de façon synchrone, sauf si vous définissez l’un des indicateurs. Si vous définissez l’indicateur TBL_BATCH, **Restrict** reporte l’évaluation de la restriction, sauf si vous demandez les données. Si l’indicateur de TBL_ASYNC est défini, **Restrict** fonctionne de manière asynchrone et peut être retourné avant la fin de l’opération.
  
Tous les signets d’une table sont ignorés lorsqu’un appel à **Restrict** est effectué, et BOOKMARK_CURRENT, la position actuelle du curseur, est définie sur le début de la table. 
  
Si vous tentez d’imposer une restriction de propriété à une propriété qui ne figure pas dans l’ensemble de colonnes de la table, les résultats ne sont pas définis. Chaque fois que vous ne savez pas si une propriété est prise en charge dans une table, combinez la restriction de propriété avec une restriction existe. La restriction existe vérifie l’existence de la propriété avant de tenter d’imposer la restriction de propriété. 
  
Ne vous attendez pas à recevoir une notification de table sur une ligne qui a été filtrée à partir d’une table en raison d’une restriction.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::ApplyRestriction  <br/> |MFCMAPI utilise la méthode **IMAPITable::Restrict** pour définir une restriction sur une table. |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

