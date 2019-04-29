---
title: IMAPITableRestrict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Restrict
api_type:
- COM
ms.assetid: a5bfc190-b58f-44c3-893c-8727df14ee58
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6cca6bc12fa6f100885b7bf705d79fa24a2e2f91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414619"
---
# <a name="imapitablerestrict"></a>IMAPITable::Restrict

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Applique un filtre à un tableau, réduisant ainsi la valeur de la ligne sur les lignes correspondant aux critères spécifiés.
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpRestriction_
  
> dans Pointeur vers une structure [SRestriction](srestriction.md) définissant les conditions du filtre. Le fait de transmettre NULL dans le paramètre _lpRestriction_ supprime le filtre actif. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le moment de l'opération de restriction. Les indicateurs suivants peuvent être définis:
    
TBL_ASYNC 
  
> Démarre l'opération de manière asynchrone et renvoie avant la fin de l'opération.
    
TBL_BATCH 
  
> Diffère l'évaluation du filtre jusqu'à ce que les données de la table soient requises.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le filtre a été appliqué.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours, ce qui empêche le démarrage de l'opération de restriction. L'opération en cours doit être autorisée ou elle doit être arrêtée.
    
MAPI_E_TOO_COMPLEX 
  
> Le tableau ne peut pas effectuer l'opération, car le filtre particulier pointé par le paramètre _lpRestriction_ est trop compliqué. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable:: Restrict** établit une restriction, ou filtre, sur une table. S'il existe une restriction précédente, elle est ignorée et la nouvelle est appliquée. L'application d'une restriction n'a aucun effet sur les données sous-jacentes d'un tableau; elle modifie simplement l'affichage en limitant les lignes pouvant être récupérées sur les lignes contenant des données qui satisfont à la restriction. 
  
Il existe plusieurs types de restrictions, chacun étant décrit par une structure différente. La structure [SRestriction](srestriction.md) contient deux membres: une valeur qui indique le type de restriction et la structure spécifique applicable à ce type. 
  
Les notifications pour les lignes de tableau masquées par les appels à **limiter** ne sont jamais générées. 
  
Une restriction de propriété sur une propriété à valeurs multiples fonctionne comme une restriction sur une propriété à valeur unique. Une propriété à valeurs multiples à utiliser dans une restriction de propriété doit avoir l'indicateur MVI_FLAG défini. Si cet indicateur n'est pas défini, il est traité comme un tuple entièrement ordonné. Une comparaison de deux colonnes à valeurs multiples compare les éléments de colonne dans l'ordre, en signalant la relation entre les colonnes à la première inégalité. L'égalité est renvoyée uniquement si les colonnes comparées contiennent les mêmes valeurs dans le même ordre. Si une colonne comporte moins de valeurs que l'autre, la relation signalée est celle d'une valeur null à l'autre valeur.
  
Pour plus d'informations sur les restrictions, consultez la rubrique [à propos des restrictions](about-restrictions.md).
  
> [!NOTE]
> Si vous créez des requêtes dynamiques pour rechercher des données sur le serveur, utilisez la méthode **FindRow** au lieu d'utiliser la méthode Restrict et la méthode **QueryRows** ensemble. **** La **** méthode Restrict crée une vue mise en cache qui est utilisée pour évaluer tous les messages ajoutés ou modifiés dans le dossier de base. Si une application cliente utilise **** la méthode Restrict pour chaque requête dynamique, une vue mise en cache est créée pour chaque requête. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour ignorer la restriction actuelle sans en créer une autre, transmettez la valeur NULL dans _lpRestriction_.
  
Si un autre appel de table asynchrone est en cours **** , entraînant le retour de MAPI_E_BUSY, vous pouvez appeler [IMAPITable:: Abort](imapitable-abort.md) pour arrêter l'appel. 
  
 La **restriction** opère de façon synchrone sauf si vous définissez l'un des indicateurs. Si vous définissez l'indicateur TBL_BATCH, **** la méthode Restrict diffère l'évaluation de la restriction, sauf si vous demandez les données. Si l'indicateur TBL_ASYNC est défini, la **restriction**fonctionne de manière asynchrone, ce qui peut renvoyer avant la fin de l'opération.
  
Tous les signets d'une table sont ignorés lorsqu'un appel à **** la fonction Restrict est effectué, et BOOKMARK_CURRENT, la position actuelle du curseur, est définie au début de la table. 
  
Si vous tentez d'imposer une restriction de propriété sur une propriété qui n'est pas dans le jeu de colonnes de la table, les résultats ne sont pas définis. Chaque fois que vous n'êtes pas sûr de savoir si une propriété est prise en charge dans un tableau, combinez la restriction de propriété avec une restriction exists. La restriction Exists vérifie l'existence de la propriété avant d'imposer la restriction de propriété. 
  
Ne prévoyez pas de recevoir une notification de table sur une ligne qui a été filtrée à partir d'une table en raison d'une restriction.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl:: ApplyRestriction  <br/> |MFCMAPI utilise la méthode **IMAPITable:: Restrict** pour définir une restriction sur un tableau.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

