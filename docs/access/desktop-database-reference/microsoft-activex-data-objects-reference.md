---
title: Référence de Microsoft ActiveX Data Objects
TOCTitle: Microsoft ActiveX Data Objects Reference
ms:assetid: 235fc575-8a2e-913c-fa3d-bb86256733f9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249010(v=office.15)
ms:contentKeyID: 48543728
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a774dc4ee20e1f97e2b77d8835abb0524881e465
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606758"
---
# <a name="microsoft-activex-data-objects-reference"></a>Référence de Microsoft ActiveX Data Objects

**S’applique à**: Access 2013 | Office 2013

## <a name="purpose"></a>Utilité

Microsoft ActiveX Data Objects (ADO) permet à vos applications clientes d'accéder et de manipuler des données à partir d'un serveur de base de données par l'intermédiaire d'un fournisseur OLE DB. Il offre de nombreux avantages dont une grande facilité d'utilisation, une vitesse élevée, une charge de mémoire faible et un encombrement disque limité. ADO prend en charge les fonctionnalités clés de création d'applications client/serveur et Web.

## <a name="rds"></a>RDS

<<<<<<< Tête ADO comprend également le Service RDS (Remote Data), à laquelle vous pouvez déplacer des données d’un serveur à une application cliente ou une page Web, manipuler les données sur le client et renvoyer les mises à jour sur le serveur dans un seul aller-retour.
=== ADO comprend également le Service RDS (Remote Data), à laquelle vous pouvez déplacer des données d’un serveur à une application cliente ou une page Web, manipuler les données sur le client et renvoyer les mises à jour sur le serveur dans un seul aller-retour.
>>>>>>> master

## <a name="ado-md"></a>ADO MD

Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) fournit un accès facile aux données multidimensionnelles issues de langages tels que Microsoft Visual Basic, Microsoft Visual C++ et Microsoft Visual J++. ADO MD est une extension de Microsoft ADO qui permet d'inclure des objets spécifiques aux données multidimensionnelles, par exemple les objets CubeDef et Cellset. Grâce à ADO MD, vous pouvez parcourir un schéma multidimensionnel, exécuter une requête relative à un cube et récupérer les résultats.

À l'instar d'ADO, ADO MD utilise un fournisseur OLE DB sous-jacent pour accéder aux données. Pour utiliser ADO MD, le fournisseur doit être un fournisseur de données multidimensionnelles (MDP), tel qu'il est défini par OLE DB pour la spécification OLAP. Les fournisseurs de données multidimensionnelles présentent les données dans des vues multidimensionnelles, contrairement aux fournisseurs de données tabulaires (TDP), qui présentent les données dans des vues tabulaires. Consultez la documentation de votre fournisseur OLAP OLE DB pour des informations détaillées sur la syntaxe et le comportement spécifiques pris en charge par votre fournisseur.

## <a name="adox"></a>ADOX

Microsoft ActiveX Data Objects Extensions pour la sécurité et le langage de définition des données (ADOX) est une extension des objets et du modèle de programmation ADO. ADOX comprend les objets utilisés pour la sécurité ainsi que pour la création et la modification des schémas. Étant donné que la manipulation des schémas repose sur des objets, vous pouvez écrire du code qui fonctionne avec plusieurs sources de données, même si leurs syntaxes natives présentent des différences.

ADOX est une bibliothèque qui complète les objets ADO de base. Il expose des objets supplémentaires destinés à la création, à la modification et à la suppression des objets de schéma, tels que les tables et procédures. Il comprend aussi des objets de sécurité, d'une part pour gérer les utilisateurs et les groupes, d'autre part pour octroyer et supprimer les autorisations d'accès aux objets.

## <a name="ado-25-main-components"></a>ADO 2.5 composants principaux

- [Guide du programmeur](ado-programmer-s-guide.md): introduction à l’aide d’ADO, RDS, ADO MD et ADOX.

- [Référence du programmeur](ado-programmer-s-reference-topics.md): cette section de la documentation ADO contient des rubriques pour chaque collection ADO, RDS, ADO MD et objet ADOX, propriété, propriété dynamique, méthode, événement et énumération.

## <a name="feedback"></a>Commentaires

Vous pouvez envoyer vos commentaires sur la documentation ou les exemples de code ADO à l'équipe concernée.

