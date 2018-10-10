---
title: Appliquer un ruban personnalisé à un formulaire ou un état
TOCTitle: Apply a custom ribbon to a form or report
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4fb0155b1a1ed36b6fe924f72a4da385197cc21
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471674"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a>Appliquer un ruban personnalisé à un formulaire ou un état


**S’applique à**: Access 2013 | Office 2013

Le ruban utilise le balisage XML déclaratif textuels qui simplifie la création et la personnalisation du ruban. Avec quelques lignes de code XML, vous pouvez créer l’interface de l’utilisateur. Access fournit la flexibilité de la personnalisation de l’interface utilisateur du ruban. Par exemple, marquage de personnalisation permettre être stockée dans une table, incorporé dans une procédure VBA, stocké dans une autre base de données Access ou liée à une feuille de calcul Excel. Cette rubrique décrit comment appliquer des rubans personnalisés lors du chargement d’un formulaire ou un état.

## <a name="making-the-ribbon-customization-xml-available"></a>Disposition de la personnalisation du ruban XML

**Stockage d’extensibilité du ruban XML dans une Table**

Une des méthodes que vous pouvez utiliser pour rendre disponibles des personnalisations de ruban consiste à stocker dans une table. Si vous stockez les personnalisations dans une table dénommée **RubansSysU**, les personnalisations peuvent être implémentées sans utiliser de macros ou du code VBA.

**RubansSysU** est une table système créée par l’utilisateur. Le tableau doit être créé en utilisant des noms de colonne spécifique afin que les personnalisations du ruban à mettre en œuvre. La table ci-dessous contient les paramètres à utiliser lors de la création de la table **RubansSysU**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom de colonne</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>Texte</p></td>
<td><p>Contient le nom du ruban personnalisé à associer à cette personnalisation</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Mémo</p></td>
<td><p>Contient le XML d’extensibilité (RibbonX) qui définit la personnalisation du ruban du ruban</p></td>
</tr>
</tbody>
</table>


**Chargement extensibilité du ruban XML par programmation**

Vous pouvez utiliser la méthode **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** pour charger les personnalisations du ruban par programme. En règle générale, pour créer le ruban et disponibles pour l’application, vous créez tout d’abord un module dans la base de données avec une procédure qui appelle la méthode **LoadCustomUI** , en passant le nom du ruban et le balisage de personnalisation XML.

Le balisage XML peut provenir d’un objet **Recordset** créé à partir d’une table, d’une source externe à la base de données, tel qu’un fichier XML que vous analysez dans une chaîne ou d’un balisage XML incorporé directement dans la procédure. Vous pouvez créer différents rubans en utilisant plusieurs appels de la méthode **LoadCustomUI** , en passant un balisage XML différent dans la mesure où le nom de chaque ruban et l’attribut **id** des onglets constituant le ruban sont uniques.

Une fois la procédure terminée, vous créez ensuite une macro AutoExec qui appelle la procédure à l'aide de l'action ExécuterCode. Ainsi, lorsque l’application est démarrée, la méthode **LoadCustomUI** s’exécute automatiquement et tous les rubans personnalisés sont accessibles à l’application.

## <a name="assigning-custom-ribbons-to-forms-or-reports"></a>Affectation de rubans personnalisés à des formulaires ou des États

1.  Suivez le processus décrit précédemment pour rendre le ruban personnalisé disponible pour cette application.

2.  Ouvrez le formulaire ou l'état en mode Création.

3.  Sous l’onglet Création, cliquez sur **Feuille de propriétés**.

4.  Sous l’onglet **Tout** de la fenêtre Propriétés, cliquez dans la liste **Nom du ruban**, puis sélectionnez un Ruban.

5.  Enregistrer, fermez et rouvrez le formulaire ou état. Le ruban de l’interface utilisateur que vous avez sélectionné est affiché.


> [!NOTE]
> Les onglets affichés dans l’interface utilisateur du ruban sont additive. Autrement dit, sauf si vous spécifiquement masquez les onglets ou définissez l’attribut *Démarrer à partir de zéro* à **la valeur True**, les onglets affichés dans un formulaire ou interface utilisateur de ruban de l’état s’ajoutent aux onglets existants.

> [!NOTE]
> [!REMARQUE] Pour plus d'informations sur l'interface du ruban dans d'autres applications Office, consultez l'article [Vue d'ensemble du ruban Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


