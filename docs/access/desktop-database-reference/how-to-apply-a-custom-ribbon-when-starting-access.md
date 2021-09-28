---
title: Appliquer un ruban personnalisé au démarrage d’Access
TOCTitle: Apply a custom ribbon when starting Access
description: Découvrez comment appliquer des rubans personnalisés lorsque vous ouvrez une base de données dans Access 2013.
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 10/16/2018
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: b52d3b261a3655eedd6a6f911d0d1eade31712aa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602387"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a>Appliquer un ruban personnalisé au démarrage d’Access

**S’applique à :** Access 2013 | Office 2013

Le ruban utilise un balisage XML déclaratif basé sur texte, qui simplifie la création et la personnalisation du ruban. Avec quelques lignes de XML, vous pouvez créer simplement l’interface idéale pour l’utilisateur. Access fournit une grande flexibilité lors de la personnalisation du ruban de l’interface utilisateur. Par exemple, un balisage de personnalisation peut être stocké dans un tableau, incorporé dans une procédure VBA, stocké dans une autre base de données Access ou lié à une feuille de calcul Excel. Découvrez comment appliquer des rubans personnalisés lorsque vous ouvrez une base de données.

## <a name="make-the-ribbon-customization-xml-available"></a>Rendre disponible la personnalisation du ruban XML

### <a name="store-ribbon-extensibility-xml-in-a-table"></a>Stocker extensibilité du ruban XML dans un tableau

Une méthode que vous pouvez utiliser pour rendre des personnalisations du ruban disponible consiste à les stocker dans un tableau. Si vous stockez les personnalisations dans un tableau nommé **USysRibbons**, les personnalisations peuvent être mises en œuvre sans utiliser des macros ou du code VBA.

**USysRibbons** est un tableau système créé par l’utilisateur. Ce tableau doit être créé en utilisant des noms de colonnes spécifiques afin que les personnalisations du ruban soient implémentées. 

Le tableau suivant répertorie les paramètres à utiliser lors de la création du tableau **USysRibbons**.

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
<td><p>Text</p></td>
<td><p>Contient le nom du ruban personnalisé devant être associé à cette personnalisation.</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Mémo</p></td>
<td><p>Contient le XML d'extensibilité du ruban (RibbonX) qui définit la personnalisation du ruban.</p></td>
</tr>
</tbody>
</table>


### <a name="load-ribbon-extensibility-xml-programmatically"></a>Charger extensibilité du ruban XML par programme

Vous pouvez utiliser la méthode **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** permettant de charger les personnalisations de ruban par programme. En règle générale, pour créer le ruban et le mettre à la disposition de l’application, vous devez tout d’abord créer un module dans la base de données avec une procédure qui appelle la méthode **LoadCustomUI**, laquelle transmet le nom du Ruban et le code de personnalisation XML.

Le code XML peut provenir d’un objet **Recordset** créé à partir d’une table, d’une source externe à la base de données (comme un fichier XML que vous analysez dans un objet de type String) ou de code XML incorporé directement dans la procédure. Vous pouvez rendre plusieurs rubans disponibles à l'aide de plusieurs appels à la méthode **LoadCustomUI**, autre balisage XML, dans la mesure où le nom de chaque ruban et l'attribut **id** des onglets constituant le ruban sont uniques.

Une fois la procédure terminée, vous créez ensuite une macro AutoExec qui appelle la procédure à l'aide de l'action ExécuterCode. Ainsi, lorsque l'application est lancée, la méthode **LoadCustomUI** s'exécute automatiquement et tous les rubans personnalisés sont accessibles par l'application.

## <a name="apply-customized-ribbons-when-access-starts"></a>Appliquer des rubans personnalisés lorsque Access démarre

Pour appliquer un ruban personnalisé disponible au démarrage de l'application, procédez comme suit :

1.  Exécutez la procédure décrite plus haut pour rendre les rubans personnalisés accessibles à l’application.

2.  Quittez et redémarrez l’application.

3.  Choisissez le **bouton Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), puis choisissez **Options Access**.

4.  Cliquez sur l'option **Base de données active**, dans la section **Options de la barre d'outils et du ruban**, puis sur la liste **Nom du ruban** et sélectionnez un ruban.

5.  Quittez et redémarrez l’application. L’interface utilisateur que vous avez sélectionnée est affichée.

> [!NOTE]
> Pour plus d'informations sur l'interface du ruban dans d'autres applications Office, consultez l'article [Vue d'ensemble du ruban Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


