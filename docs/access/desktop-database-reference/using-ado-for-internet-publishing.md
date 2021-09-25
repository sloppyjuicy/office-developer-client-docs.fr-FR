---
title: Utilisation d'ADO pour la publication Internet
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3c6ec66f838691398afbff5f4f117bf4b8cff13f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557749"
---
# <a name="using-ado-for-internet-publishing"></a>Utilisation d’ADO pour la publication Internet


**S’applique à** : Access 2013, Office 2013



Le [fournisseur OLE DB pour la publication Internet](the-ole-db-provider-for-internet-publishing.md) montre un exemple spécifique d'accès à des données hétérogènes avec ADO. Bien que les exemples de cette section soient spécifiques à l’utilisation du fournisseur de publication Internet, les principes démontrés doivent être similaires lors de l’utilisation d’ADO avec d’autres fournisseurs à des données hétérogènes, telles qu’un fournisseur vers un magasin de courrier.

## <a name="urls"></a>URL

Les URL peuvent être utilisées à la place des chaînes de connexion et du texte des commandes pour spécifier les sources de données et l'emplacement des fichiers et des répertoires. Vous pouvez les utiliser avec des objets [Connection](connection-object-ado.md) et **Recordset** existants ainsi qu'avec des objets **Record** et **Stream**.

Pour plus d'informations sur l'utilisation des URL, consultez [URL absolues et relatives](absolute-and-relative-urls.md).

## <a name="record-fields"></a>Champs d'enregistrement

La différence qui distingue les données hétérogènes des données homogènes est qu’avec les premières, chaque ligne de données, ou objet **Record**, peut comporter des jeux de colonnes différents, ou objets **Field**, alors qu’avec les secondes, chaque ligne comporte le même jeu de colonnes. Pour plus d’informations sur des champs spécifiques au fournisseur pour la publication sur Internet, voir [Enregistrements et champs spécifiques au fournisseur](records-and-provider-supplied-fields.md).

## <a name="appending-new-fields"></a>Ajout de nouveaux champs

Plusieurs objets ADO ont été améliorés pour fonctionner avec les objets **Record** et **Stream**.

  - La méthode [Append](fields-collection-ado.md) de la collection [Fields](append-method-ado.md) permet de créer et d'ajouter un objet [Field](field-object-ado.md) à la collection et peut également spécifier la valeur de l'objet **Field**.

  - La méthode [Update](update-method-ado.md) finalise l'ajout ou la suppression d'objets Field dans la collection.

  - Une autre solution plus rapide que l'utilisation de la méthode **Append** consiste à créer des champs simplement en affectant une valeur à un champ non défini ou précédemment supprimé.

## <a name="see-also"></a>Voir aussi

- [Rubriques sur le scénario de publication Internet](internet-publishing-scenario.md)
