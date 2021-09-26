---
title: CopyRecord, méthode (ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 924df406830cf5bc1547df2bee11195b7f9e3602
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589847"
---
# <a name="copyrecord-method-ado"></a>CopyRecord, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Copie une entité représentée par un objet **Record** vers un autre emplacement.

## <a name="syntax"></a>Syntaxe

*Enregistrement*. CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Source* |Facultatif. Valeur de type **String** contenant une URL spécifiant l’entité à copier (par exemple, un fichier ou un répertoire). Si le paramètre *Source* est omis ou spécifie une chaîne vide, le fichier ou le répertoire représenté par l’objet [Record](record-object-ado.md) actif est copié.|
|*Destination* |Facultatif. Valeur de type **String** contenant une URL spécifiant l'emplacement dans lequel *Source* va être copié.|
|*UserName* |Facultatif. Valeur de type **String** contenant l'ID utilisateur, qui le cas échéant, autorise l'accès à *Destination*.|
|*Password* |Facultatif. Valeur de type **String** contenant le mot de passe qui, le cas échéant, vérifie le paramètre *NomUtilisateur*.|
|*Options* |Facultatif. Valeur de l'énumération [CopyRecordOptionsEnum](copyrecordoptionsenum.md) (par défaut, **adCopyUnspecified** ). Spécifie le comportement de cette méthode.|
|*Async* |Facultatif. Valeur de type **Boolean** qui, lorsqu'elle correspond à **True**, indique que cette opération doit être asynchrone.|

## <a name="return-value"></a>Valeur renvoyée

Valeur de type **String** qui retourne, en général, la valeur de *Destination*. Toutefois, la valeur exacte renvoyée dépend du fournisseur.

## <a name="remarks"></a>Remarques

Les valeurs des paramètres *Source* et *Destination* ne doivent pas être identiques sans quoi une erreur d'exécution se produit. Il faut au moins que le nom du serveur, du chemin d'accès ou de la ressource diffère.

Tous les enfants (par exemple, les sous-répertoires) de *Source* sont copiés de manière récursive sauf si la valeur **adCopyNonRecursive** est spécifiée. Dans une opération récursive, *Destination* ne doit pas correspondre à un sous-répertoire de *Source* sans quoi l'opération n'est pas exécutée.

Cette méthode échoue si *Destination* identifie une entité existante (par exemple, un fichier ou un répertoire) sauf si **adCopyOverWrite** est spécifié.

> [!IMPORTANT]
> Soyez prudent lorsque vous utilisez l'option **adCopyOverWrite**. Si, par exemple, vous la spécifiez lors de la copie d'un fichier dans un répertoire, ce répertoire est *supprimé* et remplacé par le fichier.


> [!NOTE]
> Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, voir [URL absolues et relatives.](absolute-and-relative-urls.md)


