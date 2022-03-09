---
title: IMAPITableQueryPosition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.QueryPosition
api_type:
- COM
ms.assetid: 510b2e21-ba27-47dd-87cb-2a549e31fa28
ms.openlocfilehash: 5568c885117c85831a8351edb5dd1a6542e4da20
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373661"
---
# <a name="imapitablequeryposition"></a>IMAPITable::QueryPosition

**S’applique à** : Outlook 2013 | Outlook 2016
 
Extrait la position de ligne de tableau actuelle du curseur, en fonction d’une valeur fractionnaire.
 
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>Paramètres

 _lpulRow_
 
> [out] Pointeur vers le numéro de la ligne actuelle. Le numéro de ligne est de base zéro ; la première ligne du tableau est zéro.

 _lpulNumerator_
 
> [out] Pointeur vers le numérateur pour la fraction identifiant la position du tableau.

 _lpulDenominator_
 
> [out] Pointeur vers le dénominateur de la fraction identifiant la position du tableau. Le _paramètre lpulDenominator ne peut_ pas être zéro.

## <a name="return-value"></a>Valeur renvoyée

S_OK

> La méthode a renvoyé des valeurs valides dans _lpulRow_, _lpulNumerator_ et _lpulDenominator_.

## <a name="remarks"></a>Remarques

La **méthode IMAPITable::QueryPosition** détermine la position de ligne actuelle et renvoie le numéro de la ligne actuelle et une valeur fractionnaire indiquant sa position relative à la fin du tableau. MAPI définit la ligne actuelle comme ligne suivante à lire.
 
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous n’avez pas besoin de renvoyer le nombre exact de lignes dans la table pour le _paramètre lpulDenominator_ ; Il peut s’agit d’une estimation.
 
Si vous ne pouvez pas déterminer la ligne actuelle, renvoyez la valeur 0xFFFFFFFF dans _lpulRow_.
 
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser **QueryPosition** pour positionner une case de défilement dans une barre de défilement. Par exemple, dans un tableau de 100 lignes, si **QueryPosition** renvoie la valeur 75 dans le paramètre _lpulNumerator_ , 100 dans le paramètre _lpulDenominator_ et 75 dans le paramètre _lpulRow_ , vous pouvez positionner la case de défilement 3/4 de la manière dans la barre de défilement.
 
Ne comptez pas sur la valeur _dans lpulDenominator_ qui est le nombre de lignes dans le tableau. **QueryPosition ne** peut pas toujours identifier la ligne exacte sur la position du curseur.
 
Un appel à **QueryPosition** peut impliquer de grandes quantités de mémoire, en particulier pour les tables classées de grande taille. Si le _paramètre lpulRow_ est 0xFFFFFFFF, trop de mémoire était nécessaire pour **que QueryPosition** détermine la ligne actuelle. Appelez [la méthode IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) pour positionner la table sur la ligne identifiée par les paramètres _lpulNumerator_ et _lpulDenominator_ . Toutefois, n’attendez pas toujours que **SeekRowApprox** établisse en tant que position actuelle la même ligne **que QueryPosition** aurait si la mémoire n’avait pas été un facteur.
 
## <a name="see-also"></a>Voir aussi

[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)  
[IMAPITable : IUnknown](imapitableiunknown.md)
