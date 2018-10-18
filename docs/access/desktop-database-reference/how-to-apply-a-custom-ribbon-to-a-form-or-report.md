---
titre : appliquer un ruban personnalisé à un formulaire ou un état TOCTitle : appliquer un ruban personnalisé à un formulaire ou un état <<<<<<< ms:assetid tête : 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl : https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID : ms.date 48545865 : 18/09/2015 === === description : comment appliquer des rubans personnalisés lors du chargement d’un formulaire ou un état dans Access 2013.
MS:AssetId : 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl : https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID : ms.date 48545865 : 10/16/2018
>>>>>>> maître mtps_version : v=office.15
---

# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a>Appliquer un ruban personnalisé à un formulaire ou un état

<<<<<<< Tête

**S’applique à**: Access 2013 | Office 2013

Le ruban utilise le balisage XML déclaratif textuels qui simplifie la création et la personnalisation du ruban. Avec quelques lignes de code XML, vous pouvez créer l’interface de l’utilisateur. Access fournit la flexibilité de la personnalisation de l’interface utilisateur du ruban. Par exemple, marquage de personnalisation permettre être stockée dans une table, incorporé dans une procédure VBA, stocké dans une autre base de données Access ou liée à une feuille de calcul Excel. Cette rubrique décrit comment appliquer des rubans personnalisés lors du chargement d’un formulaire ou un état.

## <a name="making-the-ribbon-customization-xml-available"></a>Disposition de la personnalisation du ruban XML

**Stockage d’extensibilité du ruban XML dans une Table**

Une des méthodes que vous pouvez utiliser pour rendre disponibles des personnalisations de ruban consiste à stocker dans une table. Si vous stockez les personnalisations dans une table dénommée **RubansSysU**, les personnalisations peuvent être implémentées sans utiliser de macros ou du code VBA.

<a name="usysribbons-is-a-user-created-system-table-the-table-must-be-created-using-specific-column-names-in-order-for-the-ribbon-customizations-to-be-implemented-the-following-table-lists-the-settings-to-use-when-creating-the-usysribbons-table"></a>**RubansSysU** est une table système créée par l’utilisateur. Le tableau doit être créé en utilisant des noms de colonne spécifique afin que les personnalisations du ruban à mettre en œuvre. La table ci-dessous contient les paramètres à utiliser lors de la création de la table **RubansSysU**.
=======
**S’applique à**: Access 2013 | Office 2013

Le ruban utilise le balisage XML déclaratif textuels qui simplifie la création et la personnalisation du ruban. Avec quelques lignes de code XML, vous pouvez créer l’interface de l’utilisateur. Access fournit la flexibilité de la personnalisation de l’interface utilisateur du ruban. 

Par exemple, marquage de personnalisation permettre être stockée dans une table, incorporé dans une procédure VBA, stocké dans une autre base de données Access ou liée à une feuille de calcul Excel. Cette rubrique décrit comment appliquer des rubans personnalisés lors du chargement d’un formulaire ou un état.

## <a name="make-the-ribbon-customization-xml-available"></a>Disposition de la personnalisation du ruban XML

### <a name="store-ribbon-extensibility-xml-in-a-table"></a>Stocker l’extensibilité du ruban XML dans une table

Une des méthodes que vous pouvez utiliser pour rendre disponibles des personnalisations de ruban consiste à stocker dans une table. Si vous stockez les personnalisations dans une table dénommée **RubansSysU**, les personnalisations peuvent être implémentées sans utiliser de macros ou du code VBA.

**RubansSysU** est une table système créée par l’utilisateur. Le tableau doit être créé en utilisant des noms de colonne spécifiques pour les personnalisations du ruban à mettre en œuvre. 

La table ci-dessous contient les paramètres à utiliser lors de la création de la table **RubansSysU**.
>>>>>>> master

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<<<<<<< Tête
<th><p>Nom de colonne</p></th>
<th><p>Type de données</p></th>
=======
<th><p>Nom de colonne</p></th>
<th><p>Type de données</p></th>
>>>>>>>forme de base
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>Texte</p></td>
<<<<<<< Tête
<td><p>Contient le nom du ruban personnalisé à associer à cette personnalisation</p></td>
=======
<td><p>Contient le nom du ruban personnalisé devant être associé à cette personnalisation.</p></td>
>>>>>>>forme de base
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Mémo</p></td>
<<<<<<< Tête
<td><p>Contient le XML d’extensibilité (RibbonX) qui définit la personnalisation du ruban du ruban</p></td>
=======
<td><p>Contient l’extensibilité du ruban (RibbonX) XML qui définit la personnalisation du ruban.</p></td>
>>>>>>>forme de base
</tr>
</tbody>
</table>


<<<<<<< Tête de **chargement de l’extensibilité du ruban XML par programmation**

<a name="you-can-use-the-loadcustomuihttpsmsdnmicrosoftcomlibraryff194416voffice15-method-to-load-ribbon-customizations-programmatically-typically-to-create-and-make-the-ribbon-available-to-the-application-you-first-create-a-module-in-the-database-with-a-procedure-that-calls-the-loadcustomui-method-passing-in-the-name-of-the-ribbon-and-the-xml-customization-markup"></a>Vous pouvez utiliser la méthode **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** pour charger les personnalisations du ruban par programme. En règle générale, pour créer le ruban et disponibles pour l’application, vous créez tout d’abord un module dans la base de données avec une procédure qui appelle la méthode **LoadCustomUI** , en passant le nom du ruban et le balisage de personnalisation XML.
=======
### <a name="load-ribbon-extensibility-xml-programmatically"></a>Charger le code XML d’extensibilité du ruban par programme

Vous pouvez utiliser la méthode **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** pour charger les personnalisations du ruban par programme. En règle générale, pour créer le ruban et disponibles pour l’application, vous créez tout d’abord un module dans la base de données avec une procédure qui appelle la méthode **LoadCustomUI** , en passant le nom du ruban et le balisage de personnalisation XML.
>>>>>>> master

Le balisage XML peut provenir d’un objet **Recordset** créé à partir d’une table, d’une source externe à la base de données, tel qu’un fichier XML que vous analysez dans une chaîne ou d’un balisage XML incorporé directement dans la procédure. Vous pouvez créer différents rubans en utilisant plusieurs appels de la méthode **LoadCustomUI** , en passant un balisage XML différent dans la mesure où le nom de chaque ruban et l’attribut **id** des onglets constituant le ruban sont uniques.

Une fois la procédure terminée, vous créez ensuite une macro AutoExec qui appelle la procédure à l'aide de l'action ExécuterCode. Ainsi, lorsque l’application est démarrée, la méthode **LoadCustomUI** s’exécute automatiquement et tous les rubans personnalisés sont accessibles à l’application.

<<<<<<< Tête
## <a name="assigning-custom-ribbons-to-forms-or-reports"></a>Affectation de rubans personnalisés à des formulaires ou des États
=======
## <a name="assign-custom-ribbons-to-forms-or-reports"></a>Affecter des rubans personnalisés à des formulaires ou des États
>>>>>>> master

1.  Suivez le processus décrit précédemment pour rendre le ruban personnalisé disponible pour cette application.

2.  Ouvrez le formulaire ou l'état en mode Création.

<<<<<<< Tête
3.  Sous l’onglet Création, cliquez sur **Feuille de propriétés**.

4.  Sous l’onglet **Tout** de la fenêtre Propriétés, cliquez dans la liste **Nom du ruban**, puis sélectionnez un Ruban.
=======
3.  Sous l’onglet Création, cliquez sur **Feuille de propriétés**.

4.  Sous l’onglet **tous** de la fenêtre Propriétés, sélectionnez la liste **Nom du ruban** , puis sélectionnez un ruban.
>>>>>>> master

5.  Enregistrer, fermez et rouvrez le formulaire ou état. Le ruban de l’interface utilisateur que vous avez sélectionné est affiché.


> [!NOTE]
> Les onglets affichés dans l’interface utilisateur du ruban sont additive. Autrement dit, sauf si vous spécifiquement masquez les onglets ou définissez l’attribut *Démarrer à partir de zéro* à **la valeur True**, les onglets affichés dans un formulaire ou interface utilisateur de ruban de l’état s’ajoutent aux onglets existants.

> [!NOTE]
> [!REMARQUE] Pour plus d'informations sur l'interface du ruban dans d'autres applications Office, consultez l'article [Vue d'ensemble du ruban Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


