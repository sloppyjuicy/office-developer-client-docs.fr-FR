---
title: 'Chapitre 10 : Enregistrements et flux'
TOCTitle: 'Chapter 10: Records and streams'
ms:assetid: 74862096-2273-3b61-f89c-06554ccf42cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249477(v=office.15)
ms:contentKeyID: 48545663
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a47ac1f850905546651ffbdd708887bf7d74940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296492"
---
# <a name="chapter-10-records-and-streams"></a>Chapitre 10 : Enregistrements et flux

**S’applique à** : Access 2013, Office 2013

ADO fournit actuellement l'objet [Recordset](recordset-object-ado.md) comme moyen principal d'accès aux informations des sources de données, telles que les bases de données relationnelles. Toutefois, certains fournisseurs prennent en charge les objets [Record](record-object-ado.md) et [Stream](stream-object-ado.md) comme objets alternatifs ou complémentaires afin de pouvoir manipuler les données provenant d'autres fournisseurs. Pour plus d'informations sur le comportement de l'objet **Record**, consultez la documentation de votre fournisseur.

## <a name="records"></a>Enregistrements

**Les** objets d’enregistrement fonctionnent essentiellement comme des **recordset d’une** ligne. However, **Records** have limited functionality compared to **Recordsets** and they have different properties and methods.The source for the data in a **Record** object can be a command which returns one row of data from the provider. Using **Record** objects rather than **Recordset** objects to receive the results from a query that returns one row of data eliminates the overhead of instantiating the more complex **Recordset** object.

Les objets **Record** peuvent servir à d’autres fins, surtout avec des fournisseurs de sources de données autres que les bases de données relationnelles traditionnelles, par exemple le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). La plupart des informations à traiter existent non pas sous la forme de tables de base de données, mais sous la forme de messages dans les systèmes de messagerie électronique et de fichiers dans les systèmes de fichiers modernes. Les objets **Record** et **Stream** facilitent l’accès aux informations stockées dans des sources autres que les bases de données relationnelles.

**L’objet Record** peut représenter et gérer des données telles que des répertoires et des fichiers dans un système de fichiers ou des dossiers et des messages dans un système de messagerie. Dans ce cas, la source de l'objet **Record** peut être la ligne active d'un objet **Recordset** ouvert, une URL absolue ou une URL relative associée à un objet [Connection](connection-object-ado.md) ouvert.

En général, un objet **Recordset** peut être utilisé pour représenter un conteneur ou un parent, tel qu'un dossier ou un répertoire, dans une hiérarchie. Un objet **Record**, quant à lui, peut servir à retourner des informations spécifiques sur un nœud du conteneur parent, par exemple un fichier ou un document. La raison principale de l'utilisation des objets **Record** pour représenter ce type d'informations est liée au fait que les sources de ces données sont hétérogènes, c'est-à-dire que chaque objet **Record** peut avoir un jeu et un nombre différents de champs. À l'inverse, les objets **Recordset** traditionnels contenant les lignes d'une base de données sont homogènes, c'est-à-dire que chaque ligne comporte le même nombre et le même type de champs.

Pour plus d’informations sur l’utilisation de l’objet **Record** dans le traitement des données hétérogènes de fournisseurs tels que le fournisseur pour la publication Internet, consultez [Utilisation d’ADO pour la publication Internet](using-ado-for-internet-publishing.md).

## <a name="streams"></a>Flux

L'objet **Stream** permet de lire, d'écrire et de gérer un flux d'octets. Il peut s'agir d'un flux d'octets de type texte ou binaire et sa taille est limitée par les ressources du système. En général, les objets **Stream** ADO  sont utilisés pour :

- contenir le texte ou les octets qui constituent un fichier ou un message, ces objets sont en général utilisés par des fournisseurs tels que le fournisseur Microsoft OLE DB pour la publication Internet. Pour plus d'informations sur cette utilisation des objets **Stream**, consultez [Utilisation d'ADO pour la publication Internet](using-ado-for-internet-publishing.md).

Un objet **Stream** peut être ouvert sur :

- un simple fichier spécifié par une URL ;

- un champ d'un objet **Record** ou **Recordset** contenant un objet **Stream**;

- le flux par défaut d'un objet **Record** ou **Recordset** représentant un répertoire ou un fichier composé ;

- un champ de ressource contenant l'URL d'un fichier simple ;

- aucune source particulière (dans ce cas, un objet **Stream** est ouvert en mémoire et les données peuvent alors être écrites dans cet objet et enregistrées dans un autre objet **Stream** ou dans un fichier) ;

- un champ BLOB dans un objet **Recordset**.

Ce chapitre présente les rubriques suivantes :

- [Flux et persistance](streams-and-persistence.md)
- [Enregistrements et champs fournis par le fournisseur](records-and-provider-supplied-fields.md)
- [URL absolues et relatives](absolute-and-relative-urls.md)
- [Utilisation d’ADO pour la publication Internet (ADO)](using-ado-for-internet-publishing.md)
