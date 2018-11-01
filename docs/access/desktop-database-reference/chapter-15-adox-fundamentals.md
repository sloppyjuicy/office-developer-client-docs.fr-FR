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
# <a name="chapter-15-adox-fundamentals"></a>Chapitre 15 : Principes de base ADOX


**S’applique à**: Access 2013, Office 2013

Microsoft® ActiveX® Data Objects Extensions for Data Definition Language and Security (ADOX) est une extension des objets et du modèle de programmation ADO. ADOX inclut des objets destinés à créer et modifier des schémas ou encore à gérer la sécurité. Comme il s'agit d'une approche orientée objet de la manipulation de schémas, elle permet d'écrire un code fonctionnant sur diverses sources de données, indépendamment des différences que présentent les syntaxes natives.

ADOX est une bibliothèque associée aux objets ADO principaux. ADOX expose des objets supplémentaires pour la création, la modification et la suppression d'objets de schéma, tels que des tables et des procédures. Il inclut également des objets de sécurité qui permettent de gérer les utilisateurs et groupes et d'accorder et d'annuler des autorisations sur des objets.

Pour utiliser ADOX avec votre outil de développement, vous devez établir une référence à la bibliothèque de types ADOX. « Microsoft ADO Ext. for DDL and Security » est la description de la bibliothèque ADOX. « Msadox.dll » est le nom de fichier de la bibliothèque ADOX et « ADOX » est l'ID programme (ProgID). Pour plus d'informations sur la création de références à des bibliothèques, consultez la documentation de votre outil de développement.

Le fournisseur Microsoft OLE DB pour le moteur de base de données Microsoft Jet assure la prise en charge complète d'ADOX. Il se peut que certaines fonctionnalités d'ADOX ne soient pas prises en charge selon votre fournisseur de données. Pour plus d'informations sur les fonctionnalités prises en charge par le fournisseur Microsoft OLE DB pour ODBC, le fournisseur Microsoft OLE DB pour Oracle ou le fournisseur Microsoft SQL Server OLE DB, consultez le fichier LisezMoi MDAC.

Ce document suppose une connaissance pratique du langage de programmation Microsoft® Visual Basic® et une connaissance générale d'ADO. Pour plus d'informations sur ADO, consultez [Guide du programmeur ADO](ado-programmer-s-guide.md).

Ce chapitre traite de la rubrique suivante :

- [Prise en charge du fournisseur pour ADOX](provider-support-for-adox.md)

Pour plus des informations générales sur ADOX, consultez les rubriques suivantes :

- [Objets ADOX](adox-objects.md)

- [Collections ADOX](adox-collections.md)

- [Propriétés ADOX](adox-properties.md)

- [Méthodes ADOX](adox-methods.md)

- [Exemples de code ADOX](adox-code-examples.md)

