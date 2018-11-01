---
title: Appliquer un ruban personnalisé au démarrage d’Access
TOCTitle: Apply a custom ribbon when starting Access
description: Comment appliquer des rubans personnalisés lors de l’ouverture d’une base de données dans Access 2013.
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 10/16/2018
mtps_version: v=office.15
ms.openlocfilehash: 755ff8c5b8c51927de0b212b91f2a332228f0550
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881299"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a>Appliquer un ruban personnalisé au démarrage d’Access

**S’applique à :** Access 2013 | Office 2013

Le ruban utilise le balisage XML déclaratif textuels qui simplifie la création et la personnalisation du ruban. Avec quelques lignes de code XML, vous pouvez créer l’interface de l’utilisateur. Access fournit une flexibilité considérable pour personnaliser l’interface utilisateur du ruban. Par exemple, marquage de personnalisation permettre être stockée dans une table, incorporé dans une procédure VBA, stocké dans une autre base de données Access ou liée à une feuille de calcul Excel. Cette rubrique décrit comment appliquer des rubans personnalisés lors de l’ouverture d’une base de données.

## <a name="make-the-ribbon-customization-xml-available"></a>Disposition de la personnalisation du ruban XML

### <a name="store-ribbon-extensibility-xml-in-a-table"></a>Stocker l’extensibilité du ruban XML dans une table

Une des méthodes que vous pouvez utiliser pour rendre disponibles des personnalisations de ruban consiste à stocker dans une table. Si vous stockez les personnalisations dans une table dénommée **RubansSysU**, les personnalisations peuvent être implémentées sans utiliser de macros ou du code VBA.

**RubansSysU** est une table système créée par l’utilisateur. Le tableau doit être créé en utilisant des noms de colonne spécifiques pour les personnalisations du ruban à mettre en œuvre. 

La table ci-dessous contient les paramètres à utiliser lors de la création de la table **RubansSysU**.

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
<td><p>Contient le nom du ruban personnalisé devant être associé à cette personnalisation.</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Mémo</p></td>
<td><p>Contient l’extensibilité du ruban (RibbonX) XML qui définit la personnalisation du ruban.</p></td>
</tr>
</tbody>
</table>


### <a name="load-ribbon-extensibility-xml-programmatically"></a>Charger le code XML d’extensibilité du ruban par programme

Vous pouvez utiliser la méthode **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** pour charger les personnalisations du ruban par programme. En règle générale, pour créer le ruban et disponibles pour l’application, vous créez tout d’abord un module dans la base de données avec une procédure qui appelle la méthode **LoadCustomUI** , en passant le nom du ruban et le balisage de personnalisation XML.

Le balisage XML peut provenir d’un objet **Recordset** créé à partir d’une table, d’une source externe à la base de données, tel qu’un fichier XML que vous analysez dans une chaîne ou d’un balisage XML incorporé directement dans la procédure. Vous pouvez créer différents rubans en utilisant plusieurs appels de la méthode **LoadCustomUI** , en passant un balisage XML différent dans la mesure où le nom de chaque ruban et l’attribut **id** des onglets constituant le ruban sont uniques.

Une fois la procédure terminée, vous créez ensuite une macro AutoExec qui appelle la procédure à l'aide de l'action ExécuterCode. Ainsi, lorsque l’application est démarrée, la méthode **LoadCustomUI** s’exécute automatiquement et tous les rubans personnalisés sont accessibles à l’application.

## <a name="apply-customized-ribbons-when-access-starts"></a>Appliquer des rubans personnalisés au démarrage d’Access

Pour appliquer une interface utilisateur personnalisée de sorte qu’il soit disponible au démarrage de l’application, utilisez la procédure suivante :

1.  Suivez la procédure décrite précédemment pour rendre les rubans personnalisés accessibles à l’application.

2.  Fermez er redémarrez l'application.

3.  Cliquez sur le **Bouton Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") , puis sur **Options Access**.

4.  Choisissez l’option de **Base de données actuelle** puis, dans la section **Options de la barre d’outils et du ruban** , cliquez sur la liste **Nom du ruban** et sélectionnez un ruban.

5.  Maintenant, fermez et redémarrez l’application. L’interface utilisateur que vous avez sélectionné est affiché.

> [!NOTE]
> [!REMARQUE] Pour plus d'informations sur l'interface du ruban dans d'autres applications Office, consultez l'article [Vue d'ensemble du ruban Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


