---
title: Supports, méthode (ADO)
TOCTitle: Supports Method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b94c19e41031b94f75d3dd8bb58f95eab416fb48
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872591"
---
# <a name="supports-method-ado"></a>Supports, méthode (ADO)


**S’applique à**: Access 2013, Office 2013

Détermine si un objet [Recordset](recordset-object-ado.md) spécifié prend en charge un type de fonctionnalité particulier.

## <a name="syntax"></a>Syntaxe

*Boolean* = *jeu d’enregistrements*. Prend en charge (*CursorOptions*)

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur de **type Boolean** qui indique si toutes les fonctionnalités identifiées par l’argument *CursorOptions* sont prises en charge par le fournisseur.

## <a name="parameters"></a>Paramètres

  - *CursorOptions*

  - Expression de type **Long** comportant une ou plusieurs valeurs [CursorOptionEnum](cursoroptionenum.md).

## <a name="remarks"></a>Notes

Utilisez la méthode **Supports** pour déterminer les types de fonctionnalités prises en charge par un objet **Recordset**. Si l'objet **Recordset** prend en charge les fonctionnalités dont les constantes correspondantes se trouvent dans *CursorOptions*, la méthode **Supports** retourne **True**. Sinon, elle renvoie **False**.


> [!NOTE]
> <P>[!REMARQUE] Même si la méthode <STRONG>Supports</STRONG> peut retourner la valeur <STRONG>True</STRONG> pour une fonctionnalité déterminée, cela ne signifie pas pour autant que le fournisseur peut rendre la fonctionnalité disponible en toutes circonstances. La méthode <STRONG>Supports</STRONG> indique simplement si le fournisseur peut prendre en charge la fonctionnalité spécifiée, en partant du principe que certaines conditions sont remplies. Par exemple, la méthode <STRONG>Supports</STRONG> peut indiquer qu'un objet <STRONG>Recordset</STRONG> prend en charge les mises à jour même si le curseur est basé sur une jointure de plusieurs tables, dont certaines colonnes ne peuvent pas être mises à jour.</P>


