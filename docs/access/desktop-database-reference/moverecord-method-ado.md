---
title: MoveRecord, méthode (ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9937f0ab32c5dba0e4435fdc0ba7e111f5651dc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698364"
---
# <a name="moverecord-method-ado"></a>MoveRecord, méthode (ADO)

**S’applique à**: Access 2013, Office 2013
 
Déplace l'entité représentée par un objet [Record](record-object-ado.md) vers un autre emplacement.

## <a name="syntax"></a>Syntaxe

*Enregistrement*. MoveRecord (*Source*, *Destination*, *nom d’utilisateur*, *mot de passe*, *Options*, *asynchrone*)

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*Source* |Facultatif. Valeur de type **String** qui contient une URL identifiant l'objet **Record** à déplacer. Si *Source* est omis ou spécifie une chaîne vide, l'objet représenté par cet **enregistrement** est déplacé. Par exemple si l'objet **Record** représente un fichier, le contenu du fichier est déplacé vers l'emplacement spécifié par le paramètre *Destination*.|
|*Destination* |Facultatif. Une valeur de **type String** qui contient une URL spécifiant l’emplacement où seront déplacées *Source* .|
|*UserName* |Facultatif. Valeur de type **String** contenant l'ID utilisateur, qui le cas échéant, autorise l'accès à *Destination*.|
|*Password* |Facultatif. Valeur de type **String** contenant le mot de passe qui, le cas échéant, vérifie le paramètre *NomUtilisateur*.|
|*Options* |Facultatif. Valeur [MoveRecordOptionsEnum](moverecordoptionsenum.md) dont la valeur par défaut est **adMoveUnspecified**. Spécifie le comportement de cette méthode.|
|*Async* |Facultatif. **Boolean** valeur de **la valeur True**, spécifie cette opération doit être asynchrone.|

## <a name="return-value"></a>Valeur renvoyée

Valeur de type **String**. En règle générale, la valeur de *Destination* est renvoyée. Toutefois, la valeur retournée précise dépend du fournisseur.

## <a name="remarks"></a>Notes

Les valeurs de la *Source* et de *Destination* ne doivent pas être identiques ; dans le cas contraire, une erreur d’exécution se produit. Il faut au moins que les noms de ressource, de chemin d'accès et de serveur diffèrent.

Pour les fichiers déplacés à l'aide du fournisseur de la publication Internet, cette méthode met à jour tous les liens hypertexte dans les fichiers déplacés sauf indication contraire précisée dans *Options*. Cette méthode échoue si *Destination* identifie un objet existant (fichier ou répertoire, par exemple), à moins que **adMoveOverWrite** soit spécifié.

> [!NOTE]
> [!REMARQUE] Soyez prudent lorsque vous utilisez l'option **adMoveOverWrite**. Si, par exemple, vous spécifiez cette option lorsque vous déplacez un fichier vers un répertoire, le répertoire est supprimé et remplacé par le fichier.

Certains attributs de l’objet **Record** , telles que la propriété [ParentURL](parenturl-property-ado.md) , ne seront pas mis à jour une fois cette opération terminée. Actualiser les propriétés de l’objet **Record** en fermant l' **enregistrement**, puis rouvrir avec l’URL de l’emplacement où le fichier ou répertoire a été déplacé.

Si l'objet **Record** a été obtenu d'un objet [Recordset](recordset-object-ado.md), le nouvel emplacement du fichier ou répertoire déplacé n'est pas directement reflété dans l'objet **Recordset**. Actualisez l'objet **Recordset** en le fermant puis en le rouvrant.

> [!NOTE]
> [!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, consultez [URL absolues et relatives](absolute-and-relative-urls.md).


