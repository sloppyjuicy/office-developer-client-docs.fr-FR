---
title: MoveRecord, méthode (ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d5c3abebc80dea7d5871faa7926cf81bdd9a681f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606568"
---
# <a name="moverecord-method-ado"></a>MoveRecord, méthode (ADO)

**S’applique à** : Access 2013, Office 2013
 
Déplace l’entité représentée par un objet [Record](record-object-ado.md) vers un autre emplacement.

## <a name="syntax"></a>Syntaxe

*Enregistrement*. MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Source* |Facultatif. Valeur de type **String** qui contient une URL identifiant l'objet **Record** à déplacer. Si *Source* est omis ou spécifie une chaîne vide, l'objet représenté par cet **enregistrement** est déplacé. Par exemple si l'objet **Record** représente un fichier, le contenu du fichier est déplacé vers l'emplacement spécifié par le paramètre *Destination*.|
|*Destination* |Facultatif. Valeur de type **String** qui contient une URL spécifiant l'emplacement vers lequel déplacer *Source*.|
|*UserName* |Facultatif. Valeur de type **String** contenant l'ID utilisateur, qui le cas échéant, autorise l'accès à *Destination*.|
|*Password* |Facultatif. Valeur de type **String** contenant le mot de passe qui, le cas échéant, vérifie le paramètre *NomUtilisateur*.|
|*Options* |Facultatif. Valeur [MoveRecordOptionsEnum](moverecordoptionsenum.md) dont la valeur par défaut est **adMoveUnspecified**. Spécifie le comportement de cette méthode.|
|*Async* |Facultatif. Valeur **boolénaire** qui, lorsque la valeur **est True,** spécifie que cette opération doit être asynchrone.|

## <a name="return-value"></a>Valeur renvoyée

Valeur de type **String**. En général, il s'agit de la valeur de *Destination*. Toutefois, la valeur retournée précise dépend du fournisseur.

## <a name="remarks"></a>Remarques

Les valeurs de *Source* et *Destination* ne peuvent pas être identiques sans quoi une erreur d'exécution se produit. Il faut au moins que les noms de ressource, de chemin d'accès et de serveur diffèrent.

Pour les fichiers déplacés à l'aide du fournisseur de la publication Internet, cette méthode met à jour tous les liens hypertexte dans les fichiers déplacés sauf indication contraire précisée dans *Options*. Cette méthode échoue si *Destination* identifie un objet existant (fichier ou répertoire, par exemple), à moins que **adMoveOverWrite** soit spécifié.

> [!NOTE]
> [!REMARQUE] Soyez prudent lorsque vous utilisez l'option **adMoveOverWrite**. Si, par exemple, vous spécifiez cette option lorsque vous déplacez un fichier vers un répertoire, le répertoire est supprimé et remplacé par le fichier.

Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes. Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.

Si l’objet **Record** a été obtenu d’un objet [Recordset](recordset-object-ado.md), le nouvel emplacement du fichier ou répertoire déplacé n’est pas directement reflété dans l’objet **Recordset**. Actualisez l’objet **Recordset** en le fermant puis en le rouvrant.

> [!NOTE]
> Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, voir [URL absolues et relatives.](absolute-and-relative-urls.md)


