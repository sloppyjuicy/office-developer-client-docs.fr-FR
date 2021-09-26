---
title: 'Chapitre 15 : Principes de base ADOX'
TOCTitle: 'Chapter 15: ADOX fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 952599694588c5535d8d6d9e205e45d67b8b3020
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627092"
---
# <a name="chapter-15-adox-fundamentals"></a>Chapitre 15 : Principes de base ADOX

**S’applique à** : Access 2013, Office 2013

Microsoft ActiveX Data Objects Extensions pour la sécurité et le langage de définition des données (ADOX) est une extension des objets et du modèle de programmation ADO. ADOX comprend les objets utilisés pour la sécurité ainsi que pour la création et la modification des schémas. Étant donné que la manipulation des schémas repose sur des objets, vous pouvez écrire du code qui fonctionne avec plusieurs sources de données, même si leurs syntaxes natives présentent des différences.

ADOX est une bibliothèque qui complète les objets ADO de base. Il expose des objets supplémentaires destinés à la création, à la modification et à la suppression des objets de schéma, tels que les tables et procédures. Il comprend aussi des objets de sécurité, d'une part pour gérer les utilisateurs et les groupes, d'autre part pour octroyer et supprimer les autorisations d'accès aux objets.

Pour utiliser ADOX avec votre outil de développement, vous devez établir une référence à la bibliothèque de types ADOX. « Microsoft ADO Ext. for DDL and Security » est la description de la bibliothèque ADOX. « Msadox.dll » est le nom de fichier de la bibliothèque ADOX et « ADOX » est l'ID programme (ProgID). Pour plus d'informations sur la création de références à des bibliothèques, consultez la documentation de votre outil de développement.

Le fournisseur Microsoft OLE DB pour le moteur de base de données Microsoft Jet assure la prise en charge complète d'ADOX. Il se peut que certaines fonctionnalités d'ADOX ne soient pas prises en charge selon votre fournisseur de données. Pour plus d'informations sur les fonctionnalités prises en charge par le fournisseur Microsoft OLE DB pour ODBC, le fournisseur Microsoft OLE DB pour Oracle ou le fournisseur Microsoft SQL Server OLE DB, consultez le fichier LisezMoi MDAC.

Ce document suppose une connaissance approfondie du langage de programmation microsoft Visual Basic et une connaissance générale d’ADO. Pour plus d’informations sur ADO, voir le guide du [programmeur ADO.](ado-programmer-s-guide.md)

Ce chapitre traite de la rubrique suivante :

- [Prise en charge du fournisseur pour ADOX](provider-support-for-adox.md)

Pour plus des informations générales sur ADOX, consultez les rubriques suivantes :

- [Objets ADOX](adox-objects.md)
- [Collections ADOX](adox-collections.md)
- [Propriétés ADOX](adox-properties.md)
- [Méthodes ADOX](adox-methods.md)
- [Exemples ADOX](adox-code-examples.md)

