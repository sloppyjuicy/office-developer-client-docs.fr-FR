---
title: Seek, méthode - ActiveX Data Objects (ADO)
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: bdf15631bc1897158e5efab5712434a5ef61eb07
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580874"
---
# <a name="seek-method-ado"></a>Seek, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Effectue une recherche dans l’index d’un objet [Recordset](recordset-object-ado.md) pour retrouver rapidement la ligne qui correspond aux valeurs spécifiées et faire de cette ligne la position de ligne active.

## <a name="syntax"></a>Syntaxe

*recordset*. Seek *KeyValues*, *SeekOption*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*KeyValues* |Tableau de valeurs de type **Variant**. Un index se compose d'une ou plusieurs colonnes et le tableau contient une valeur à comparer à chaque colonne correspondante.|
|*SeekOption* |Valeur [SeekEnum](seekenum.md) qui spécifie le type de comparaison à effectuer entre les colonnes de l’index et les *ValeursClés* correspondantes.|

## <a name="remarks"></a>Remarques

Il est conseillé d’utiliser conjointement la méthode **Seek** avec la propriété [Index](index-property-ado.md) si le fournisseur sous-jacent prend les index en charge sur l’objet **Recordset**. La méthode [Supports](supports-method-ado.md)**(adSeek)** permet de déterminer si le fournisseur sous-jacent prend **Seek** en charge, et la méthode **Supports(adIndex)** de déterminer si les index sont pris en charge par le fournisseur. (Par exemple, le [fournisseur OLE DB pour Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) prend **Seek** et **Index** en charge.)

Si la méthode **Seek** ne trouve pas la ligne recherchée, aucune erreur n'est générée et la ligne est positionnée à la fin du **Recordset**. Veillez à définir la propriété **Index** sur l'index souhaité avant d'exécuter cette méthode.

Cette méthode n'est prise en charge qu'avec les curseurs côté serveur. Seek n'est pas prise en charge lorsque la valeur de la propriété **CursorLocation** de l'objet [Recordset](cursorlocation-property-ado.md) est **adUseClient**.

Vous ne pouvez employer cette méthode que dans le seul cas où l'objet **Recordset** a été ouvert avec une valeur [adCmdTableDirect](commandtypeenum.md) pour **CommandTypeEnum**.

