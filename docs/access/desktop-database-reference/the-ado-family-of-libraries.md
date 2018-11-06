---
title: La famille de bibliothèques ADO
TOCTitle: The ADO family of libraries
ms:assetid: 9e794509-d0a8-2e5b-02a8-65e26f059c4e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249724(v=office.15)
ms:contentKeyID: 48546656
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 821de4312d3fa76468311305b18eaaa156e05318
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999042"
---
# <a name="the-ado-family-of-libraries"></a>La famille de bibliothèques ADO

**S’applique à**: Access 2013, Office 2013

La famille ADO est constituée de trois bibliothèques principales : ADO (y compris RDS), ADO MD et ADOX.

## <a name="ado"></a>ADO

ADO permet à vos applications clientes d'accéder et de manipuler des données à partir d'un serveur de base de données par l'intermédiaire d'un fournisseur OLE DB. Il offre de nombreux avantages dont une grande facilité d'utilisation, une vitesse élevée, une charge de mémoire faible et un encombrement disque limité. ADO prend en charge les fonctionnalités clés pour la création d’applications web et client/serveur.

ADO comprend également le Service RDS (Remote Data), à laquelle vous pouvez déplacer des données d’un serveur à une application cliente ou une page Web, manipuler les données sur le client et renvoyer les mises à jour sur le serveur dans un seul aller-retour.

## <a name="ado-md"></a>ADO MD

Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) fournit un accès facile aux données multidimensionnelles issues de langages, tels que Microsoft Visual Basic, Microsoft Visual C++ et Microsoft Visual J++. ADO MD est une extension d'ADO, qui permet d'inclure des objets spécifiques aux données multidimensionnelles, par exemple les objets **CubeDef** et **Cellset**. Grâce à ADO MD, vous pouvez parcourir un schéma multidimensionnel, exécuter une requête relative à un cube et récupérer les résultats.

À l'instar d'ADO, ADO MD utilise un fournisseur OLE DB sous-jacent pour accéder aux données. Pour utiliser ADO MD, le fournisseur doit être un fournisseur de données multidimensionnelles (MDP), tel qu'il est défini par OLE DB pour la spécification OLAP. Les fournisseurs de données multidimensionnelles présentent les données dans des vues multidimensionnelles, contrairement aux fournisseurs de données tabulaires (TDP), qui présentent les données dans des vues tabulaires. Pour obtenir des informations détaillées sur la syntaxe et le comportement spécifiques pris en charge par votre fournisseur, consultez la documentation de votre fournisseur OLE DB pour OLAP .

## <a name="adox"></a>ADOX

Microsoft ActiveX Data Objects Extensions pour la sécurité et le langage de définition des données (ADOX) est une extension des objets et du modèle de programmation ADO. ADOX comprend les objets utilisés pour la sécurité ainsi que pour la création et la modification des schémas. Étant donné que la manipulation des schémas repose sur des objets, vous pouvez écrire du code qui fonctionne avec plusieurs sources de données, même si leurs syntaxes natives présentent des différences.

ADOX est une bibliothèque qui complète les objets ADO de base. Il expose des objets supplémentaires destinés à la création, à la modification et à la suppression des objets de schéma, tels que les tables et procédures. Il comprend aussi des objets de sécurité, d'une part pour gérer les utilisateurs et les groupes, d'autre part pour octroyer et supprimer les autorisations d'accès aux objets.

