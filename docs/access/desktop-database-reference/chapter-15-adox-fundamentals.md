---
title: 'Chapitre 15 : Principes de base ADOX'
TOCTitle: 'Chapter 15: ADOX Fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 72152a67a9846adacbc6b200a3517c7e65b9fc4c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881908"
---
# <a name="chapter-15-adox-fundamentals"></a><span data-ttu-id="82702-102">Chapitre 15 : Principes de base ADOX</span><span class="sxs-lookup"><span data-stu-id="82702-102">Chapter 15: ADOX Fundamentals</span></span>


<span data-ttu-id="82702-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="82702-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="82702-p101">Microsoft® ActiveX® Data Objects Extensions for Data Definition Language and Security (ADOX) est une extension des objets et du modèle de programmation ADO. ADOX inclut des objets destinés à créer et modifier des schémas ou encore à gérer la sécurité. Comme il s'agit d'une approche orientée objet de la manipulation de schémas, elle permet d'écrire un code fonctionnant sur diverses sources de données, indépendamment des différences que présentent les syntaxes natives.</span><span class="sxs-lookup"><span data-stu-id="82702-p101">Microsoft® ActiveX® Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification, as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="82702-p102">ADOX est une bibliothèque associée aux objets ADO principaux. ADOX expose des objets supplémentaires pour la création, la modification et la suppression d'objets de schéma, tels que des tables et des procédures. Il inclut également des objets de sécurité qui permettent de gérer les utilisateurs et groupes et d'accorder et d'annuler des autorisations sur des objets.</span><span class="sxs-lookup"><span data-stu-id="82702-p102">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

<span data-ttu-id="82702-p103">Pour utiliser ADOX avec votre outil de développement, vous devez établir une référence à la bibliothèque de types ADOX. « Microsoft ADO Ext. for DDL and Security » est la description de la bibliothèque ADOX. « Msadox.dll » est le nom de fichier de la bibliothèque ADOX et « ADOX » est l'ID programme (ProgID). Pour plus d'informations sur la création de références à des bibliothèques, consultez la documentation de votre outil de développement.</span><span class="sxs-lookup"><span data-stu-id="82702-p103">To use ADOX with your development tool, you should establish a reference to the ADOX type library. The description of the ADOX library is "Microsoft ADO Ext. for DDL and Security." The ADOX library file name is Msadox.dll, and the program ID (ProgID) is "ADOX". For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="82702-p104">Le fournisseur Microsoft OLE DB pour le moteur de base de données Microsoft Jet assure la prise en charge complète d'ADOX. Il se peut que certaines fonctionnalités d'ADOX ne soient pas prises en charge selon votre fournisseur de données. Pour plus d'informations sur les fonctionnalités prises en charge par le fournisseur Microsoft OLE DB pour ODBC, le fournisseur Microsoft OLE DB pour Oracle ou le fournisseur Microsoft SQL Server OLE DB, consultez le fichier LisezMoi MDAC.</span><span class="sxs-lookup"><span data-stu-id="82702-p104">The Microsoft OLE DB Provider for the Microsoft Jet Database Engine fully supports ADOX. Certain features of ADOX may not be supported, depending on your data provider. For more information about supported features with the Microsoft OLE DB Provider for ODBC, the Microsoft OLE DB Provider for Oracle, or the Microsoft SQL Server OLE DB Provider, see the MDAC readme file.</span></span>

<span data-ttu-id="82702-117">Ce document suppose une connaissance pratique du langage de programmation Microsoft® Visual Basic® et une connaissance générale d'ADO.</span><span class="sxs-lookup"><span data-stu-id="82702-117">This document assumes a working knowledge of the Microsoft® Visual Basic® programming language and a general knowledge of ADO.</span></span> <span data-ttu-id="82702-118">Pour plus d'informations sur ADO, consultez [Guide du programmeur ADO](ado-programmer-s-guide.md).</span><span class="sxs-lookup"><span data-stu-id="82702-118">For more information about ADO, see the [ADO Programmer's Guide](ado-programmer-s-guide.md).</span></span>

<span data-ttu-id="82702-119">Ce chapitre traite de la rubrique suivante :</span><span class="sxs-lookup"><span data-stu-id="82702-119">This chapter covers the following topic:</span></span>

- [<span data-ttu-id="82702-120">Prise en charge du fournisseur pour ADOX</span><span class="sxs-lookup"><span data-stu-id="82702-120">Provider Support for ADOX</span></span>](provider-support-for-adox.md)

<span data-ttu-id="82702-121">Pour plus des informations générales sur ADOX, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="82702-121">For more overview information about ADOX, see the following topics:</span></span>

- [<span data-ttu-id="82702-122">Objets ADOX</span><span class="sxs-lookup"><span data-stu-id="82702-122">ADOX Objects</span></span>](adox-objects.md)

- [<span data-ttu-id="82702-123">Collections ADOX</span><span class="sxs-lookup"><span data-stu-id="82702-123">ADOX Collections</span></span>](adox-collections.md)

- [<span data-ttu-id="82702-124">Propriétés ADOX</span><span class="sxs-lookup"><span data-stu-id="82702-124">ADOX Properties</span></span>](adox-properties.md)

- [<span data-ttu-id="82702-125">Méthodes ADOX</span><span class="sxs-lookup"><span data-stu-id="82702-125">ADOX Methods</span></span>](adox-methods.md)

- [<span data-ttu-id="82702-126">Exemples de code ADOX</span><span class="sxs-lookup"><span data-stu-id="82702-126">ADOX Examples</span></span>](adox-code-examples.md)

