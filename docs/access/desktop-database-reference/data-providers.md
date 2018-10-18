---
title: Fournisseurs de données (référence de base de données du bureau Access)
TOCTitle: Data Providers
ms:assetid: c1e36245-4ece-4986-db30-dc4be3daa794
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249946(v=office.15)
ms:contentKeyID: 48547540
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4eab9679b09b31b01250372df294af55729e9dd9
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604539"
---
# <a name="data-providers"></a><span data-ttu-id="59108-102">Fournisseurs de données</span><span class="sxs-lookup"><span data-stu-id="59108-102">Data Providers</span></span>


<span data-ttu-id="59108-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="59108-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="59108-p101">Les fournisseurs de données représentent diverses sources de données, telles que les bases de données SQL, les fichiers séquentiels indexés, les feuilles de calcul, les magasins de documents et les fichiers de courrier. Leurs données sont exposées de façon uniforme en utilisant une abstraction commune appelée groupe de lignes.</span><span class="sxs-lookup"><span data-stu-id="59108-p101">Data providers represent diverse sources of data such as SQL databases, indexed-sequential files, spreadsheets, document stores, and mail files. Providers expose data uniformly using a common abstraction called the rowset.</span></span>

<span data-ttu-id="59108-p102">ADO est puissant et flexible car il peut se connecter à plusieurs fournisseurs de données tout en exposant le même modèle de programmation, quelles que soient les fonctionnalités propres à chaque fournisseur. Cependant, chaque fournisseur de données étant unique, le mode d'interaction de votre application avec ADO varie en fonction du fournisseur de données.</span><span class="sxs-lookup"><span data-stu-id="59108-p102">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider. However, because each data provider is unique, how your application interacts with ADO will vary by data provider.</span></span>

<span data-ttu-id="59108-108"><<<<<<< Tête par exemple, les fonctionnalités du fournisseur OLE DB pour SQL Server, qui est utilisée pour accéder aux bases de données Microsoft SQL Server, sont très différentes de celles du fournisseur Microsoft OLE DB pour Internet Publication, qui est utilisé pour accéder au fichier stocke sur un serveur Web.</span><span class="sxs-lookup"><span data-stu-id="59108-108"><<<<<<< HEAD For example, the capabilities and features of the OLE DB Provider for SQL Server, which is used to access Microsoft SQL Server databases, are considerably different from those of the Microsoft OLE DB Provider for Internet Publishing, which is used to access file stores on a Web server.</span></span>
<span data-ttu-id="59108-109">=== Par exemple, les fonctionnalités du fournisseur OLE DB pour SQL Server, qui est utilisée pour accéder aux bases de données Microsoft SQL Server, sont très différentes de celles du fournisseur Microsoft OLE DB pour la publication Internet, qui est utilisé pour l’accès magasins de fichiers sur un serveur web.</span><span class="sxs-lookup"><span data-stu-id="59108-109">======= For example, the capabilities and features of the OLE DB Provider for SQL Server, which is used to access Microsoft SQL Server databases, are considerably different from those of the Microsoft OLE DB Provider for Internet Publishing, which is used to access file stores on a web server.</span></span>
>>>>>>> <span data-ttu-id="59108-110">master</span><span class="sxs-lookup"><span data-stu-id="59108-110">master</span></span>

