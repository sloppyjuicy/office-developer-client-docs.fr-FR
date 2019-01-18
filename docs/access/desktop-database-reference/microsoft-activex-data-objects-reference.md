---
title: Référence des objets ADO (ActiveX Data Objects) Microsoft
TOCTitle: Microsoft ActiveX Data Objects Reference
ms:assetid: 235fc575-8a2e-913c-fa3d-bb86256733f9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249010(v=office.15)
ms:contentKeyID: 48543728
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c1fee657c0d6ecd319157f704df2b1c5a900be3b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698882"
---
# <a name="microsoft-activex-data-objects-reference"></a><span data-ttu-id="a0936-102">Référence des objets ADO (ActiveX Data Objects) Microsoft</span><span class="sxs-lookup"><span data-stu-id="a0936-102">Microsoft ActiveX Data Objects reference</span></span>

<span data-ttu-id="a0936-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0936-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="purpose"></a><span data-ttu-id="a0936-104">Utilité</span><span class="sxs-lookup"><span data-stu-id="a0936-104">Purpose</span></span>

<span data-ttu-id="a0936-105">Microsoft ActiveX Data Objects (ADO) permet à vos applications clientes d'accéder et de manipuler des données à partir d'un serveur de base de données par l'intermédiaire d'un fournisseur OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a0936-105">Microsoft ActiveX Data Objects (ADO) enable your client applications to access and manipulate data from a database server through an OLE DB provider.</span></span> <span data-ttu-id="a0936-106">Il offre de nombreux avantages dont une grande facilité d'utilisation, une vitesse élevée, une charge de mémoire faible et un encombrement disque limité.</span><span class="sxs-lookup"><span data-stu-id="a0936-106">Its primary benefits are ease of use, high speed, low memory overhead, and a small disk footprint.</span></span> <span data-ttu-id="a0936-107">ADO prend en charge les fonctionnalités clés pour la création d’applications web et client/serveur.</span><span class="sxs-lookup"><span data-stu-id="a0936-107">ADO supports key features for building client/server and web-based applications.</span></span>

## <a name="rds"></a><span data-ttu-id="a0936-108">RDS</span><span class="sxs-lookup"><span data-stu-id="a0936-108">RDS</span></span>

<span data-ttu-id="a0936-109">ADO comprend également le Service RDS (Remote Data), à laquelle vous pouvez déplacer des données d’un serveur à une application cliente ou une page Web, manipuler les données sur le client et renvoyer les mises à jour sur le serveur dans un seul aller-retour.</span><span class="sxs-lookup"><span data-stu-id="a0936-109">ADO also features Remote Data Service (RDS), by which you can move data from a server to a client application or webpage, manipulate the data on the client, and return updates to the server in a single round trip.</span></span>

## <a name="ado-md"></a><span data-ttu-id="a0936-110">ADO MD</span><span class="sxs-lookup"><span data-stu-id="a0936-110">ADO MD</span></span>

<span data-ttu-id="a0936-p102">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) fournit un accès facile aux données multidimensionnelles issues de langages tels que Microsoft Visual Basic, Microsoft Visual C++ et Microsoft Visual J++. ADO MD est une extension de Microsoft ADO qui permet d'inclure des objets spécifiques aux données multidimensionnelles, par exemple les objets CubeDef et Cellset. Grâce à ADO MD, vous pouvez parcourir un schéma multidimensionnel, exécuter une requête relative à un cube et récupérer les résultats.</span><span class="sxs-lookup"><span data-stu-id="a0936-p102">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the CubeDef and Cellset objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="a0936-p103">À l'instar d'ADO, ADO MD utilise un fournisseur OLE DB sous-jacent pour accéder aux données. Pour utiliser ADO MD, le fournisseur doit être un fournisseur de données multidimensionnelles (MDP), tel qu'il est défini par OLE DB pour la spécification OLAP. Les fournisseurs de données multidimensionnelles présentent les données dans des vues multidimensionnelles, contrairement aux fournisseurs de données tabulaires (TDP), qui présentent les données dans des vues tabulaires. Consultez la documentation de votre fournisseur OLAP OLE DB pour des informations détaillées sur la syntaxe et le comportement spécifiques pris en charge par votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a0936-p103">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLAP OLE DB provider for more detailed information on the specific syntax and behaviors supported by your provider.</span></span>

## <a name="adox"></a><span data-ttu-id="a0936-118">ADOX</span><span class="sxs-lookup"><span data-stu-id="a0936-118">ADOX</span></span>

<span data-ttu-id="a0936-p104">Microsoft ActiveX Data Objects Extensions pour la sécurité et le langage de définition des données (ADOX) est une extension des objets et du modèle de programmation ADO. ADOX comprend les objets utilisés pour la sécurité ainsi que pour la création et la modification des schémas. Étant donné que la manipulation des schémas repose sur des objets, vous pouvez écrire du code qui fonctionne avec plusieurs sources de données, même si leurs syntaxes natives présentent des différences.</span><span class="sxs-lookup"><span data-stu-id="a0936-p104">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification, as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="a0936-p105">ADOX est une bibliothèque qui complète les objets ADO de base. Il expose des objets supplémentaires destinés à la création, à la modification et à la suppression des objets de schéma, tels que les tables et procédures. Il comprend aussi des objets de sécurité, d'une part pour gérer les utilisateurs et les groupes, d'autre part pour octroyer et supprimer les autorisations d'accès aux objets.</span><span class="sxs-lookup"><span data-stu-id="a0936-p105">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

## <a name="ado-25-main-components"></a><span data-ttu-id="a0936-125">ADO 2.5 composants principaux</span><span class="sxs-lookup"><span data-stu-id="a0936-125">ADO 2.5 main components</span></span>

- <span data-ttu-id="a0936-126">[Guide du programmeur](ado-programmer-s-guide.md): introduction à l’aide d’ADO, RDS, ADO MD et ADOX.</span><span class="sxs-lookup"><span data-stu-id="a0936-126">[Programmer's guide](ado-programmer-s-guide.md): An introduction to using ADO, RDS, ADO MD, and ADOX.</span></span>

- <span data-ttu-id="a0936-127">[Référence du programmeur](ado-programmer-s-reference-topics.md): cette section de la documentation ADO contient des rubriques pour chaque collection ADO, RDS, ADO MD et objet ADOX, propriété, propriété dynamique, méthode, événement et énumération.</span><span class="sxs-lookup"><span data-stu-id="a0936-127">[Programmer's reference](ado-programmer-s-reference-topics.md): This section of the ADO documentation contains topics for each ADO, RDS, ADO MD, and ADOX object, collection, property, dynamic property, method, event, and enumeration.</span></span>

## <a name="feedback"></a><span data-ttu-id="a0936-128">Commentaires</span><span class="sxs-lookup"><span data-stu-id="a0936-128">Feedback</span></span>

<span data-ttu-id="a0936-129">Vous pouvez envoyer vos commentaires sur la documentation ou les exemples de code ADO à l'équipe concernée.</span><span class="sxs-lookup"><span data-stu-id="a0936-129">You can send feedback about ADO documentation or samples directly to the ADO documentation team.</span></span>

