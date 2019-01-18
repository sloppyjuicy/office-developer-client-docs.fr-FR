---
title: Record, objet (ADO)
TOCTitle: Record object (ADO)
ms:assetid: 817aaf13-78d4-1134-aa94-997e92077c22
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249557(v=office.15)
ms:contentKeyID: 48545952
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 96ddc7fc1a93543f0eea2b42a3d423ec25a00636
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721506"
---
# <a name="record-object-ado"></a>Record, objet (ADO)


**S’applique à**: Access 2013, Office 2013

Représente une ligne d'un [Recordset](recordset-object-ado.md) ou du fournisseur de données, ou un objet renvoyé par un fournisseur de données semi-structurées, comme un fichier ou un répertoire.

## <a name="remarks"></a>Notes

Un objet **Record** représente une ligne de données et partage des similarités de concept avec un **Recordset** monoligne. Selon les fonctionnalités offertes par le fournisseur, les objets **Record** peuvent être renvoyés directement par le fournisseur pour générer un **Recordset** à une seule ligne, par exemple lorsqu'une requête SQL ne sélectionnant qu'une ligne est exécutée. Il en est de même d'un objet **Record** qui peut être obtenu directement à partir d'un objet **Recordset**. Un **Record** peut aussi être renvoyé directement depuis un fournisseur pour fournir des données semi-structurées, comme c'est le cas avec le fournisseur Microsoft Exchange OLE DB.

Vous pouvez afficher les champs associés à l'objet **Record** par l'intermédiaire de la collection [Fields](fields-collection-ado.md) de l'objet **Record**. 8373ADO accepte l'emploi de colonnes dont les valeurs sont des objets, notamment **Recordset** ou **SafeArray** ou des valeurs scalaires, dans la collection **Fields** des objets **Record**.

Si l'objet **Record** représente une ligne dans un **Recordset**, il est alors possible de revenir à ce **Recordset** d'origine avec la propriété [Source](source-property-ado-record.md).

L'objet **Record** peut également être utilisé par des fournisseurs de données semi-structurées comme [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md), pour modéliser des espaces de noms hiérarchiques. Chaque nœud de l'arborescence est un objet **Record** avec ses colonnes associées. Ces colonnes peuvent représenter les attributs de ce nœud et d'autres informations pertinentes. L'objet **Record** peut représenter un nœud feuille et un nœud branche dans l'arborescence. Les nœuds branche possèdent d'autres nœuds comme contenu, contrairement aux nœuds feuille. Ces derniers contiennent en général des flux binaires de données alors que les nœuds branche peuvent être associés à un flux binaire par défaut. Les propriétés de l'objet **Record** identifient le type de nœud.

L'objet **Record** peut aussi servir à naviguer dans des données organisées de manière hiérarchique. Un objet **Record** peut être créé pour représenter la racine d'une sous-arborescence spécifique dans une arborescence plus large, de nouveaux objets **Record** pouvant être ouverts pour représenter des nœuds enfants.

Une ressource (par exemple, un fichier ou un répertoire) peut être identifiée de manière unique par une URL absolue. Un objet [Connection](connection-object-ado.md) est créé de manière implicite et défini sur l'objet **Record** quand cet objet **Record** est ouvert avec une URL absolue. Un objet **Connection** peut être défini de manière explicite sur l'objet **Record** via la propriété [ActiveConnection](activeconnection-property-ado.md). Les fichiers et répertoires accessibles via l’objet **Connection** définissent le *contexte* dans lequel les opérations **d’enregistrement** peuvent se produire.

Les méthodes de navigation et de modification des données portant sur l'objet **Record** acceptent également les URL relatives, qui localisent une ressource à l'aide d'une URL absolue ou du contexte de l'objet **Connection** comme point de départ.

> [!NOTE]
> [!REMARQUE] Les URL qui utilisent le modèle http appellent automatiquement [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, consultez [URL absolues et relatives](absolute-and-relative-urls.md).



Un objet **Connection** est associé à chaque objet **Record**. Par conséquent, les opérations sur les objets **Record** peuvent faire partie d'une transaction faisant appel aux méthodes de transaction des objets **Connection**.

L'objet **Record** ne prend pas en charge les événements ADO et ne peut donc répondre aux notifications.

Les méthodes et les propriétés d'un objet **Record** vous permettent d'effectuer diverses tâches :

  - définir ou renvoyer l'objet **Connection** associé à l'aide de la propriété [ActiveConnection](activeconnection-property-ado.md) ;

  - indiquer les autorisations d'accès à l'aide de la propriété [Mode](mode-property-ado.md) ;

  - renvoyer l'URL du répertoire qui (le cas échéant) contient la ressource représentée par l'objet **Record**, à l'aide de la propriété [ParentURL](parenturl-property-ado.md) ;

  - indiquer l'URL absolue, l'URL relative ou l'objet **Recordset** dont provient l'objet **Record** au moyen de la propriété [Source](source-property-ado-record.md) ;

  - indiquer l'état actuel de l'objet **Record** à l'aide de la propriété [State](state-property-ado.md) ;

  - indiquer le type d’objet **Record** (*simple*, *collection* ou *document structuré*) à l’aide de la propriété [RecordType](recordtype-property-ado.md) ;

  - arrêter l'exécution d'une opération asynchrone à l'aide de la méthode [Cancel](cancel-method-ado.md) ;

  - dissocier l'objet **Record** d'une source de données à l'aide de la méthode [Close](close-method-ado.md) ;

  - copier le fichier ou le répertoire représenté par un objet **Record** dans un autre emplacement à l'aide de la méthode [CopyRecord](copyrecord-method-ado.md) ;

  - supprimer le fichier, ou le répertoire et ses sous-répertoires, représenté par un objet **Record**, à l'aide de la méthode [DeleteRecord](deleterecord-method-ado.md) ;

  - ouvrir un **Recordset** contenant des lignes qui représentent les sous-répertoires et les fichiers de l'entité représentée par l'objet **Record**, à l'aide de la méthode [GetChildren](getchildren-method-ado.md) ;

  - déplacer (renommer) le fichier, ou le répertoire et ses sous-répertoires, représenté par l'objet **Record** vers un autre emplacement, à l'aide de la méthode [MoveRecord](moverecord-method-ado.md) ;

  - associer l'objet **Record** à une source de données existante, ou créer un nouveau fichier ou répertoire, à l'aide de la méthode [Open](open-method-ado-record.md).

