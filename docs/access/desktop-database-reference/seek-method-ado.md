---
title: Seek, méthode - ActiveX Data Objects (ADO)
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ee2dbaf7dd3a15cf6cd415af208ec10a14fc9c9b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923377"
---
# <a name="seek-method-ado"></a>Seek, méthode (ADO)


**S’applique à**: Access 2013, Office 2013



Effectue une recherche dans l'index d'un objet [Recordset](recordset-object-ado.md) pour retrouver rapidement la ligne qui correspond aux valeurs spécifiées et faire de cette ligne la position de ligne active.

## <a name="syntax"></a>Syntaxe

*jeu d’enregistrements*. Seek*KeyValues*, *SeekOption*

## <a name="parameters"></a>Paramètres

  - *KeyValues*

  - Tableau de valeurs de type **Variant**. Un index se compose d'une ou plusieurs colonnes et le tableau contient une valeur à comparer à chaque colonne correspondante.

  - *SeekOption*

  - Valeur [SeekEnum](seekenum.md) qui spécifie le type de comparaison à effectuer entre les colonnes de l’index et les *ValeursClés* correspondantes.

## <a name="remarks"></a>Notes

Il est conseillé d'utiliser conjointement la méthode **Seek** avec la propriété [Index](index-property-ado.md) si le fournisseur sous-jacent prend en charge les index sur l'objet **Recordset**. Utilisez la méthode **(adSeek)** [prend en charge](supports-method-ado.md)pour déterminer si le fournisseur sous-jacent prend en charge la **méthode Seek**et la méthode **supports (adIndex)** pour déterminer si le fournisseur prend en charge les index. (Par exemple, le [fournisseur OLE DB pour Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) prend **Seek** et **Index** en charge.)

Si la méthode **Seek** ne trouve pas la ligne recherchée, aucune erreur n'est générée et la ligne est positionnée à la fin du **Recordset**. Veillez à définir la propriété **Index** sur l'index souhaité avant d'exécuter cette méthode.

Cette méthode n'est prise en charge qu'avec les curseurs côté serveur. Seek n'est pas prise en charge lorsque la valeur de la propriété **CursorLocation** de l'objet [Recordset](cursorlocation-property-ado.md) est **adUseClient**.

Vous ne pouvez employer cette méthode que dans le seul cas où l'objet **Recordset** a été ouvert avec une valeur [adCmdTableDirect](commandtypeenum.md) pour **CommandTypeEnum**.

