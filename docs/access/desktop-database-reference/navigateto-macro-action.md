---
title: NavigateTo, action de macro
TOCTitle: NavigateTo macro action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7da3eb87e775a6b02694910cd017c9535fde1df7
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998279"
---
# <a name="navigateto-macro-action"></a>NavigateTo, action de macro

**S’applique à**: Access 2013, Office 2013

Utilisez l'action **AccéderA** pour contrôler l'affichage des objets de base de données dans le volet de navigation. Vous pouvez par exemple modifier le classement des objets de base de données et appliquer un filtre aux objets de sorte que seuls certains d'entre eux soient affichés.

## <a name="setting"></a>Valeur

L'action **AccéderA** possède les arguments suivants.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Catégorie</strong></p></td>
<td><p>Obligatoire. Catégorie dans laquelle les objets doivent être affichés dans le volet de navigation. Cliquez sur <strong>Type d’objet</strong>, <strong>Tables et vues</strong>, <strong>Modifié le</strong>, <strong>Créé le</strong> ou <strong>Personnalisé</strong> dans la zone <strong>Catégorie</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Group</strong></p></td>
<td><p>Facultatif. L’argument <strong>groupe</strong> limite les objets de la catégorie s’affichent dans le volet de Navigation. Si vous laissez l’argument <strong>groupe</strong> vide, le volet de Navigation affiche tous les objets de base de données, classés selon les critères que vous spécifiez dans l’argument <strong>catégorie</strong> . Des exemples d'arguments  <strong>Groupe</strong> valides pour les différents arguments <strong>Catégorie</strong> sont répertoriés dans le tableau ci-après.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

- Cette action équivaut à sélectionner des catégories et des groupes dans la barre de titre du volet de navigation.

- La validité des arguments **Groupe** dépend de l'argument **Catégorie** utilisé. Si vous entrez un argument **Groupe** non valide, un message d'erreur s'affiche.Le tableau ci-dessous contient des exemples d'arguments **Groupe** valides pour chaque argument **Catégorie**.
    
  <table>
  <colgroup>
  <col style="width: 50%" />
  <col style="width: 50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th><p>Argument Catégorie</p></th>
  <th><p>Exemples d’arguments Groupe</p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td><p>Type d'objet</p></td>
  <td><p>Tables, Formulaires, Requêtes, Pages, Macros, Modules</p></td>
  </tr>
  <tr class="even">
  <td><p>Tables et affichages</p></td>
  <td><p>Noms de tables donnés dans la base de données</p></td>
  </tr>
  <tr class="odd">
  <td><p>Modifié le</p></td>
  <td><p>Aujourd'hui, Hier, Le mois dernier, Avant le mois dernier</p></td>
  </tr>
  <tr class="even">
  <td><p>Créé le</p></td>
  <td><p>Aujourd’hui, Hier, Le mois dernier, Avant le mois dernier</p></td>
  </tr>
  <tr class="odd">
  <td><p>Catégorie personnalisée</p></td>
  <td><p>Noms des groupes que vous avez créés pour la catégorie personnalisée spécifiée</p></td>
  </tr>
  </tbody>
  </table>

- Pour exécuter l'action **AccéderA** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **NavigateTo** de l'objet **DoCmd**.

> [!NOTE]
> [!REMARQUE] Pour accéder au niveau supérieur d'une catégorie ( **Toutes les tables**, **Tous les objets Access** ou **Toutes les dates**, par exemple), vous devez laisser l'argument Groupe vide. Par exemple, lorsque l'argument **Catégorie** est défini sur **Type d'objet**, choisir **Tous les objets Access** en tant qu'argument **Groupe** génère une erreur.


