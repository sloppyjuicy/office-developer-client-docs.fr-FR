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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3ab069728f872d82246e8925c5ad35c07f41f02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784101"
---
# <a name="imapitablerestrict"></a>IMAPITable

  
  
**S’applique à**: Outlook 
  
Applique un filtre à une table, réduisant la ligne valeur uniquement les lignes correspondant aux critères spécifiés.
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpRestriction_
  
> [in] Pointeur vers une structure [SRestriction](srestriction.md) définissant les conditions du filtre. Passage de NULL dans le paramètre _lpRestriction_ supprime le filtre actif. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le minutage de l’opération de restriction. Les indicateurs suivants peuvent être définis :
    
TBL_ASYNC 
  
> Démarre l’opération asynchrone et renvoie avant la fin de l’opération.
    
TBL_BATCH 
  
> Diffère l’évaluation du filtre jusqu'à ce que les données dans le tableau sont requises.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le filtre a été appliqué.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche l’opération de restriction de démarrage. L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.
    
MAPI_E_TOO_COMPLEX 
  
> Le tableau ne peut pas effectuer l’opération car le filtre particulier indiqué par le paramètre _lpRestriction_ est trop compliqué. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable** établit une restriction ou le filtre sur une table. S’il existe une restriction précédente, elle est ignorée et la nouvelle stratégie appliquée. Appliquer une restriction n’a aucun effet sur les données sous-jacentes d’un tableau ; Il modifie simplement l’affichage en limitant les lignes qui peuvent être récupérées aux lignes contenant des données qui répondent à la restriction. 
  
Il existe plusieurs types de restrictions, chacun décrit avec une structure différente. La structure [SRestriction](srestriction.md) contient deux membres : une valeur qui indique le type de restriction et la structure spécifique applicable pour ce type. 
  
Notifications pour les lignes de tableau qui sont masqués par les appels à **restreindre** ne sont jamais générées. 
  
Une restriction de propriété sur une propriété à valeurs multiples fonctionne comme une restriction sur une propriété à valeur unique. Une propriété à valeurs multiples à être utilisé dans une restriction de propriété doit avoir l’indicateur MVI_FLAG. Si elle ne possède pas cet indicateur est défini, il est traité comme un tuple totalement triée. Une comparaison de deux colonnes à valeurs multiples compare les éléments de la colonne dans l’ordre, la relation entre les colonnes de la première inégalité de création de rapports. Égalité est renvoyée uniquement si les colonnes comparées contiennent les mêmes valeurs dans le même ordre. Si une colonne a moins de valeurs à l’autre, la relation signalée est celui d’une valeur null à l’autre valeur.
  
Pour plus d’informations sur les restrictions, voir [à propos des Restrictions](about-restrictions.md).
  
> [!NOTE]
> Si vous créez des requêtes dynamiques pour rechercher des données sur le serveur, utilisez la méthode **FindRow** au lieu d’utiliser la méthode **Restrict** et la méthode **QueryRows** ensemble. La méthode **Restrict** crée un affichage mis en cache qui est utilisé pour analyser tous les messages ajoutés à ou modifiés dans le dossier de base. Si une application cliente utilise la méthode **Restrict** pour chaque requête dynamique, un affichage mis en cache sera créé pour chaque requête. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour supprimer la restriction actuelle sans créer un nouveau, passez la valeur NULL dans _lpRestriction_.
  
Si un autre appel asynchrone table est en cours, à l’origine **Restrict** renvoyer MAPI_E_BUSY, vous pouvez appeler [IMAPITable::Abort](imapitable-abort.md) pour arrêter l’appel. 
  
 **Restrict** fonctionne de manière synchrone, sauf si vous définissez un des indicateurs. Si vous définissez l’indicateur TBL_BATCH, **Restrict** diffère de l’évaluation de la restriction, sauf si vous demandez les données. Si l’indicateur TBL_ASYNC est défini, **Restrict**fonctionne de manière asynchrone, potentiellement renvoi avant la fin de l’opération.
  
Tous les signets pour une table sont ignorées lorsqu’un appel à **restreindre** et BOOKMARK_CURRENT, l’emplacement du curseur, est définie au début de la table. 
  
Si vous tentez d’imposer une restriction de propriété sur une propriété qui n’est pas dans l’ensemble de colonnes de la table, les résultats ne sont pas définis. Chaque fois que vous n’êtes pas certain si une propriété est prise en charge dans un tableau, combiner la restriction de propriété avec une restriction d’existe. La restriction vérifie l’existence de la propriété avant d’essayer d’imposer la restriction de propriété d’existe. 
  
Ne prévoyez pas de recevoir une notification de tableau sur une ligne qui a été filtrée d’une table en raison d’une restriction.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::ApplyRestriction  <br/> |MFCMAPI utilise la méthode **IMAPITable** pour définir une restriction sur une table.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

