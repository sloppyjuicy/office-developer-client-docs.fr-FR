---
title: SelectObject, action de macro
TOCTitle: SelectObject macro action
ms:assetid: a90539a0-c5a0-e997-9c25-e0972d28f2a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821420(v=office.15)
ms:contentKeyID: 48546914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm41840
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6287bc8a66858d51d65c37477eed7a86cd7839af
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721849"
---
# <a name="selectobject-macro-action"></a>SelectObject, action de macro

**S’applique à**: Access 2013, Office 2013

Vous pouvez utiliser l'action **SélectionnerObjet** pour sélectionner un objet de base de données spécifique.

## <a name="setting"></a>Valeur

L'action **SélectionnerObjet** accepte les arguments suivants.

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
<td><p><strong>Type d'objet</strong></p></td>
<td><p>Type d’objet de base de données à sélectionner. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Cet argument est obligatoire.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de l'objet</strong></p></td>
<td><p>Nom de l’objet à sélectionner. La zone <strong>Nom de l’objet</strong> montre tous les objets de la base de données du type sélectionné par l’argument <strong>Type d’objet</strong>. Cet argument est obligatoire sauf si vous attribuez la valeur <strong>Oui</strong> à l’argument Dans le volet de navigation.</p><p><strong>Remarque</strong>: les noms d’objets pour les objets <STRONG>Vue serveur</STRONG>, <STRONG>schéma</STRONG>ou <STRONG>Procédure stockée</STRONG> ne sont pas affichés dans la zone <STRONG>Nom de l’objet</STRONG> d’un projet Access (.adp).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dans le volet de navigation</strong></p></td>
<td><p>Spécifie si Microsoft Office Access sélectionne l’objet dans le volet de navigation. Cliquez sur <strong>Oui</strong> (pour sélectionner l’objet dans le volet de navigation) ou sur <strong>Non</strong> (pour ne pas le sélectionner). <strong>Non</strong> est la valeur par défaut.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

L'action **SélectionnerObjet** fonctionne avec n'importe quel objet Access qui peut recevoir le focus. Cette action active (ou place le focus sur) l'objet spécifié et affiche l'objet s'il est masqué. Si l'objet est un formulaire, l'action **SélectionnerObjet** définit la propriété **Visible** du formulaire sur **Oui** et retourne le formulaire dans le mode défini par ses propriétés de formulaire (par exemple, sous la forme d'un formulaire modal ou d'un formulaire contextuel).

Si l'objet n'est pas ouvert dans une des autres fenêtres Access, vous pouvez le sélectionner dans le volet de navigation en attribuant à l'argument **Dans le volet de navigation** la valeur **Oui**. Si l'argument **Dans le volet de navigation** a la valeur **Non**, un message d'erreur s'affiche lorsque vous essayez de sélectionner un objet qui n'est pas ouvert.

Cette action est souvent utilisée pour sélectionner un objet sur lequel vous voulez effectuer des actions supplémentaires. Si Access est configuré pour utiliser des fenêtres superposées au lieu de documents à onglets, vous pouvez, par exemple, restaurer un objet qui a été réduit (avec l'action **RestaurerFenêtre** ) ou agrandir une fenêtre contenant un objet que vous voulez manipuler (avec l'action **AgrandirFenêtre** ).

Si vous sélectionnez un formulaire, vous pouvez utiliser les actions **AtteindreContrôle**, **AtteindreEnregistrement** et **AtteindrePage** pour accéder à des zones spécifiques du formulaire. L'action **AtteindreEnregistrement** fonctionne également avec les feuilles de données.

Pour exécuter l'action **SélectionnerObjet** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **SelectObject** de l'objet **DoCmd**.

