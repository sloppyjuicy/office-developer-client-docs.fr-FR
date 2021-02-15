---
title: 'Chapitre 15 : Principes de base ADOX'
TOCTitle: 'Chapter 15: ADOX fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e46920ba47dba018944768ff61c970781e37a02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296450"
---
# <a name="chapter-15-adox-fundamentals"></a><span data-ttu-id="9988d-102">Chapitre 15 : Principes de base ADOX</span><span class="sxs-lookup"><span data-stu-id="9988d-102">Chapter 15: ADOX fundamentals</span></span>

<span data-ttu-id="9988d-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9988d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9988d-p101">Microsoft ActiveX Data Objects Extensions pour la sécurité et le langage de définition des données (ADOX) est une extension des objets et du modèle de programmation ADO. ADOX comprend les objets utilisés pour la sécurité ainsi que pour la création et la modification des schémas. Étant donné que la manipulation des schémas repose sur des objets, vous pouvez écrire du code qui fonctionne avec plusieurs sources de données, même si leurs syntaxes natives présentent des différences.</span><span class="sxs-lookup"><span data-stu-id="9988d-p101">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification, as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="9988d-p102">ADOX est une bibliothèque qui complète les objets ADO de base. Il expose des objets supplémentaires destinés à la création, à la modification et à la suppression des objets de schéma, tels que les tables et procédures. Il comprend aussi des objets de sécurité, d'une part pour gérer les utilisateurs et les groupes, d'autre part pour octroyer et supprimer les autorisations d'accès aux objets.</span><span class="sxs-lookup"><span data-stu-id="9988d-p102">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

<span data-ttu-id="9988d-p103">Pour utiliser ADOX avec votre outil de développement, vous devez établir une référence à la bibliothèque de types ADOX. « Microsoft ADO Ext. for DDL and Security » est la description de la bibliothèque ADOX. « Msadox.dll » est le nom de fichier de la bibliothèque ADOX et « ADOX » est l'ID programme (ProgID). Pour plus d'informations sur la création de références à des bibliothèques, consultez la documentation de votre outil de développement.</span><span class="sxs-lookup"><span data-stu-id="9988d-p103">To use ADOX with your development tool, you should establish a reference to the ADOX type library. The description of the ADOX library is "Microsoft ADO Ext. for DDL and Security." The ADOX library file name is Msadox.dll, and the program ID (ProgID) is "ADOX". For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="9988d-p104">Le fournisseur Microsoft OLE DB pour le moteur de base de données Microsoft Jet assure la prise en charge complète d'ADOX. Il se peut que certaines fonctionnalités d'ADOX ne soient pas prises en charge selon votre fournisseur de données. Pour plus d'informations sur les fonctionnalités prises en charge par le fournisseur Microsoft OLE DB pour ODBC, le fournisseur Microsoft OLE DB pour Oracle ou le fournisseur Microsoft SQL Server OLE DB, consultez le fichier LisezMoi MDAC.</span><span class="sxs-lookup"><span data-stu-id="9988d-p104">The Microsoft OLE DB Provider for the Microsoft Jet Database Engine fully supports ADOX. Certain features of ADOX may not be supported, depending on your data provider. For more information about supported features with the Microsoft OLE DB Provider for ODBC, the Microsoft OLE DB Provider for Oracle, or the Microsoft SQL Server OLE DB Provider, see the MDAC readme file.</span></span>

<span data-ttu-id="9988d-117">Ce document suppose une connaissance approfondie du langage de programmation microsoft Visual Basic et une connaissance générale d’ADO.</span><span class="sxs-lookup"><span data-stu-id="9988d-117">This document assumes a working knowledge of the Microsoft Visual Basic programming language and a general knowledge of ADO.</span></span> <span data-ttu-id="9988d-118">Pour plus d’informations sur ADO, voir le guide du [programmeur ADO.](ado-programmer-s-guide.md)</span><span class="sxs-lookup"><span data-stu-id="9988d-118">For more information about ADO, see the [ADO programmer's guide](ado-programmer-s-guide.md).</span></span>

<span data-ttu-id="9988d-119">Ce chapitre couvre la rubrique suivante :</span><span class="sxs-lookup"><span data-stu-id="9988d-119">This chapter covers the following topic:</span></span>

- [<span data-ttu-id="9988d-120">Prise en charge du fournisseur pour ADOX</span><span class="sxs-lookup"><span data-stu-id="9988d-120">Provider support for ADOX</span></span>](provider-support-for-adox.md)

<span data-ttu-id="9988d-121">Pour plus des informations générales sur ADOX, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="9988d-121">For more overview information about ADOX, see the following topics:</span></span>

- [<span data-ttu-id="9988d-122">Objets ADOX</span><span class="sxs-lookup"><span data-stu-id="9988d-122">ADOX objects</span></span>](adox-objects.md)
- [<span data-ttu-id="9988d-123">Collections ADOX</span><span class="sxs-lookup"><span data-stu-id="9988d-123">ADOX collections</span></span>](adox-collections.md)
- [<span data-ttu-id="9988d-124">Propriétés ADOX</span><span class="sxs-lookup"><span data-stu-id="9988d-124">ADOX properties</span></span>](adox-properties.md)
- [<span data-ttu-id="9988d-125">Méthodes ADOX</span><span class="sxs-lookup"><span data-stu-id="9988d-125">ADOX methods</span></span>](adox-methods.md)
- [<span data-ttu-id="9988d-126">Exemples ADOX</span><span class="sxs-lookup"><span data-stu-id="9988d-126">ADOX examples</span></span>](adox-code-examples.md)

