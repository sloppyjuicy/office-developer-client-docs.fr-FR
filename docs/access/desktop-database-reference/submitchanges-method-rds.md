---
title: Méthode SubmitChanges (RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: edb6ff720966045d411b55a723435181171b4ec6
ms.sourcegitcommit: 7c1e7389b18d4f067a69b992ac6c876b5e0441b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2022
ms.locfileid: "67365578"
---
# <a name="submitchanges-method-rds"></a>Méthode SubmitChanges (RDS)

**S’applique à** : Access 2013, Office 2013

Envoie les modifications en attente de l’objet [Recordset](recordset-object-ado.md) actualisable et placé dans le cache local à la source de données spécifiée dans la propriété [Connect](connect-property-rds.md) de la propriété [URL](url-property-rds.md).

## <a name="syntax"></a>Syntaxe

*DataControl*. SubmitChanges

*DataFactory*. SubmitChanges *Connection*, *Recordset*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*DataControl* |Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).|
|*DataFactory* |Variable objet représentant un objet [RDSServer.DataFactory](datafactory-object-rdsserver.md).|
|*Connection* |Valeur de type **String** représentant la connexion créée avec la propriété **Connect** de l'objet **RDS.DataControl**.|
|*Recordset* |Variable objet représentant un objet **Recordset**.|

## <a name="remarks"></a>Remarques

Les propriétés [Connect](connect-property-rds.md), [Server](server-property-rds.md) et [SQL](/office/vba/access/concepts/miscellaneous/sql-property-ado) doivent être définies avant de pouvoir utiliser la méthode **SubmitChanges** avec l’objet **RDS.DataControl**.

Si vous appelez la méthode [CancelUpdate](cancelupdate-method-rds.md) après avoir appelé **SubmitChanges** pour le même objet **Recordset**, l’appel **CancelUpdate** échoue car les modifications ont déjà été validées.

Seuls les enregistrements modifiés sont envoyés pour modification. Par ailleurs, soit toutes les modifications aboutissent, soit elles échouent toutes.

Vous pouvez utiliser **SubmitChanges** uniquement avec l’objet **RDSServer.DataFactory** *par défaut*. Les objets métier personnalisés ne peuvent pas utiliser cette méthode.

Si la propriété **URL** a été définie, **SubmitChanges** envoie les modifications à l'emplacement indiqué par l'URL.

