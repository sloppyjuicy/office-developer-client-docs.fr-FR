---
title: Référence des objets ADO (ActiveX Data Objects) Microsoft
TOCTitle: Microsoft ActiveX Data Objects Reference
ms:assetid: 235fc575-8a2e-913c-fa3d-bb86256733f9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249010(v=office.15)
ms:contentKeyID: 48543728
ms.date: 09/18/2021
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 0a6e7090b1be0e5c31d670e7ff5c524f8c68e8cb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606610"
---
# <a name="microsoft-activex-data-objects-reference"></a>Référence des objets ADO (ActiveX Data Objects) Microsoft

**S’applique à** : Access 2013, Office 2013

## <a name="purpose"></a>Objectif

Microsoft ActiveX Data Objects (ADO) permet à vos applications clientes d'accéder et de manipuler des données à partir d'un serveur de base de données par l'intermédiaire d'un fournisseur OLE DB. Il offre de nombreux avantages dont une grande facilité d'utilisation, une vitesse élevée, une charge de mémoire faible et un encombrement disque limité. ADO prend en charge les fonctionnalités clés de création d'applications client/serveur et Web.

## <a name="rds"></a>Services Bureau à distance

ADO comprend également la fonctionnalité RDS (Remote Data Service), grâce à laquelle vous pouvez déplacer des données d'un serveur vers une application cliente ou une page Web, manipuler les données sur le client et retourner des mises à jour au serveur en une seule boucle.

## <a name="ado-md"></a>ADO MD

Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) fournit un accès facile aux données multidimensionnelles issues de langages tels que Microsoft Visual Basic, Microsoft Visual C++ et Microsoft Visual J++. ADO MD est une extension de Microsoft ADO qui permet d'inclure des objets spécifiques aux données multidimensionnelles, par exemple les objets CubeDef et Cellset. Grâce à ADO MD, vous pouvez parcourir un schéma multidimensionnel, exécuter une requête relative à un cube et récupérer les résultats.

À l'instar d'ADO, ADO MD utilise un fournisseur OLE DB sous-jacent pour accéder aux données. Pour utiliser ADO MD, le fournisseur doit être un fournisseur de données multidimensionnelles (MDP), tel qu'il est défini par OLE DB pour la spécification OLAP. Les fournisseurs de données multidimensionnelles présentent les données dans des vues multidimensionnelles, contrairement aux fournisseurs de données tabulaires (TDP), qui présentent les données dans des vues tabulaires. Consultez la documentation de votre fournisseur OLAP OLE DB pour des informations détaillées sur la syntaxe et le comportement spécifiques pris en charge par votre fournisseur.

## <a name="adox"></a>ADOX

Microsoft ActiveX Data Objects Extensions pour la sécurité et le langage de définition des données (ADOX) est une extension des objets et du modèle de programmation ADO. ADOX comprend les objets utilisés pour la sécurité ainsi que pour la création et la modification des schémas. Étant donné que la manipulation des schémas repose sur des objets, vous pouvez écrire du code qui fonctionne avec plusieurs sources de données, même si leurs syntaxes natives présentent des différences.

ADOX est une bibliothèque qui complète les objets ADO de base. Il expose des objets supplémentaires destinés à la création, à la modification et à la suppression des objets de schéma, tels que les tables et procédures. Il comprend aussi des objets de sécurité, d'une part pour gérer les utilisateurs et les groupes, d'autre part pour octroyer et supprimer les autorisations d'accès aux objets.

## <a name="ado-25-main-components"></a>Principaux composants ADO 2.5

- [Guide du programmeur](ado-programmer-s-guide.md) : Introduction à l'utilisation de Microsoft ADO, RDS, ADO MD et ADOX.

- [Référence du programmeur](ado-programmer-s-reference-topics.md) : Cette section de la documentation ADO contient des rubriques pour chaque objet, collection, propriété, propriété dynamique, méthode, événement et énumération d'ADO, RDS, ADO MD et ADOX.
