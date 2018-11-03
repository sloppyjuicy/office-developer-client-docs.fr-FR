---
title: La famille de bibliothèques ADO
TOCTitle: The ADO family of libraries
ms:assetid: 9e794509-d0a8-2e5b-02a8-65e26f059c4e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249724(v=office.15)
ms:contentKeyID: 48546656
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4d37ef012e6db60c4a92267c82664694ed63afe
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936510"
---
# <a name="the-ado-family-of-libraries"></a><span data-ttu-id="682d4-102">La famille de bibliothèques ADO</span><span class="sxs-lookup"><span data-stu-id="682d4-102">The ADO family of libraries</span></span>

<span data-ttu-id="682d4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="682d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="682d4-104">La famille ADO est constituée de trois bibliothèques principales : ADO (y compris RDS), ADO MD et ADOX.</span><span class="sxs-lookup"><span data-stu-id="682d4-104">Three major libraries make up the ADO family: ADO (including RDS), ADO MD, and ADOX.</span></span>

## <a name="ado"></a><span data-ttu-id="682d4-105">ADO</span><span class="sxs-lookup"><span data-stu-id="682d4-105">ADO</span></span>

<span data-ttu-id="682d4-p101">ADO permet à vos applications clientes d'accéder et de manipuler des données à partir d'un serveur de base de données par l'intermédiaire d'un fournisseur OLE DB. Il offre de nombreux avantages dont une grande facilité d'utilisation, une vitesse élevée, une charge de mémoire faible et un encombrement disque limité. ADO prend en charge les fonctionnalités clés de création d'applications client/serveur et Web.</span><span class="sxs-lookup"><span data-stu-id="682d4-p101">ADO enables your client applications to access and manipulate data from a database server through an OLE DB provider. The primary benefits of ADO are ease of use, high speed, low memory overhead, and a small disk footprint. ADO supports key features for building client/server and Web-based applications.</span></span>

<span data-ttu-id="682d4-109">ADO comprend également le Service RDS (Remote Data), à laquelle vous pouvez déplacer des données d’un serveur à une application cliente ou une page Web, manipuler les données sur le client et renvoyer les mises à jour sur le serveur dans un seul aller-retour.</span><span class="sxs-lookup"><span data-stu-id="682d4-109">ADO also features Remote Data Service (RDS), by which you can move data from a server to a client application or webpage, manipulate the data on the client, and return updates to the server in a single round trip.</span></span>

## <a name="ado-md"></a><span data-ttu-id="682d4-110">ADO MD</span><span class="sxs-lookup"><span data-stu-id="682d4-110">ADO MD</span></span>

<span data-ttu-id="682d4-p102">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) fournit un accès facile aux données multidimensionnelles issues de langages, tels que Microsoft Visual Basic, Microsoft Visual C++ et Microsoft Visual J++. ADO MD est une extension d'ADO, qui permet d'inclure des objets spécifiques aux données multidimensionnelles, par exemple les objets **CubeDef** et **Cellset**. Grâce à ADO MD, vous pouvez parcourir un schéma multidimensionnel, exécuter une requête relative à un cube et récupérer les résultats.</span><span class="sxs-lookup"><span data-stu-id="682d4-p102">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends ADO to include objects specific to multidimensional data, such as the **CubeDef** and **Cellset** objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="682d4-p103">À l'instar d'ADO, ADO MD utilise un fournisseur OLE DB sous-jacent pour accéder aux données. Pour utiliser ADO MD, le fournisseur doit être un fournisseur de données multidimensionnelles (MDP), tel qu'il est défini par OLE DB pour la spécification OLAP. Les fournisseurs de données multidimensionnelles présentent les données dans des vues multidimensionnelles, contrairement aux fournisseurs de données tabulaires (TDP), qui présentent les données dans des vues tabulaires. Pour obtenir des informations détaillées sur la syntaxe et le comportement spécifiques pris en charge par votre fournisseur, consultez la documentation de votre fournisseur OLE DB pour OLAP .</span><span class="sxs-lookup"><span data-stu-id="682d4-p103">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLE DB for OLAP provider for more detailed information about the specific syntax and behaviors supported by your provider.</span></span>

## <a name="adox"></a><span data-ttu-id="682d4-118">ADOX</span><span class="sxs-lookup"><span data-stu-id="682d4-118">ADOX</span></span>

<span data-ttu-id="682d4-p104">Microsoft ActiveX Data Objects Extensions pour la sécurité et le langage de définition des données (ADOX) est une extension des objets et du modèle de programmation ADO. ADOX comprend les objets utilisés pour la sécurité ainsi que pour la création et la modification des schémas. Étant donné que la manipulation des schémas repose sur des objets, vous pouvez écrire du code qui fonctionne avec plusieurs sources de données, même si leurs syntaxes natives présentent des différences.</span><span class="sxs-lookup"><span data-stu-id="682d4-p104">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="682d4-p105">ADOX est une bibliothèque qui complète les objets ADO de base. Il expose des objets supplémentaires destinés à la création, à la modification et à la suppression des objets de schéma, tels que les tables et procédures. Il comprend aussi des objets de sécurité, d'une part pour gérer les utilisateurs et les groupes, d'autre part pour octroyer et supprimer les autorisations d'accès aux objets.</span><span class="sxs-lookup"><span data-stu-id="682d4-p105">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups, and to grant and revoke permissions on objects.</span></span>

