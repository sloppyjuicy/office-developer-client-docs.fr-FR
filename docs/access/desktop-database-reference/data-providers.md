---
title: Fournisseurs de données (référence de base de données du bureau Access)
TOCTitle: Data Providers
ms:assetid: c1e36245-4ece-4986-db30-dc4be3daa794
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249946(v=office.15)
ms:contentKeyID: 48547540
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b4b3497493627f5446055d50e525882e5187807
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886157"
---
# <a name="data-providers"></a>Fournisseurs de données


**S’applique à**: Access 2013, Office 2013

Les fournisseurs de données représentent diverses sources de données, telles que les bases de données SQL, les fichiers séquentiels indexés, les feuilles de calcul, les magasins de documents et les fichiers de courrier. Leurs données sont exposées de façon uniforme en utilisant une abstraction commune appelée groupe de lignes.

ADO est puissant et flexible car il peut se connecter à plusieurs fournisseurs de données tout en exposant le même modèle de programmation, quelles que soient les fonctionnalités propres à chaque fournisseur. Cependant, chaque fournisseur de données étant unique, le mode d'interaction de votre application avec ADO varie en fonction du fournisseur de données.

Par exemple, les fonctionnalités du fournisseur OLE DB pour SQL Server, qui est utilisée pour accéder aux bases de données Microsoft SQL Server, sont très différentes de celles du fournisseur Microsoft OLE DB pour la publication Internet, qui est utilisé pour accéder au fichier banques sur un serveur web.

