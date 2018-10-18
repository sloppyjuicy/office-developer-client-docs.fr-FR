---
titre : masquer le ruban au démarrage d’Access TOCTitle : masquer le ruban au démarrage d’Access <<<<<<< ms:assetid tête : f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl : https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID : ms.date 48548817 : 18/09/2015 === Description : comment charger un ruban personnalisé qui masque tous les onglets intégrés dans Access 2013.
MS:AssetId : f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl : https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID : ms.date 48548817 : 10/16/2018
>>>>>>> maître mtps_version : v=office.15
---

# <a name="hide-the-ribbon-when-access-starts"></a>Masquer le ruban au démarrage d’Access

**S’applique à :** Access 2013 | Office 2013

Par défaut, Microsoft Access ne fournit pas de méthode pour masquer le ruban. Cette rubrique décrit comment charger un ruban personnalisé qui masque tous les onglets prédéfinis.

Pour charger le ruban personnalisé au démarrage d'Access, vous devez stocker ses paramètres dans une table dénommée **RubansSysU**.

<<<<<<< Tête la table **RubansSysU** doit être créée à l’aide des noms de colonne spécifique afin que les personnalisations du ruban à mettre en œuvre. La table ci-dessous contient les paramètres à utiliser lors de la création de la table **RubansSysU**.
=== La table **RubansSysU** doit être créée en utilisant des noms de colonne spécifiques pour les personnalisations du ruban à mettre en œuvre. 

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
<td><p>Contient le nom du ruban personnalisé devant être associé à cette personnalisation.</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Mémo</p></td>
<<<<<<< Tête
<td><p>Contient le XML d'extensibilité du ruban (RibbonX) qui définit la personnalisation du ruban.</p></td>
=======
<td><p>Contient l’extensibilité du ruban (RibbonX) XML qui définit la personnalisation du ruban.</p></td>
>>>>>>>forme de base
</tr>
</tbody>
</table>

<<<<<<< Tête

La table contient les paramètres de personnalisation du ruban à stocker dans la table **RubansSysU**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom de colonne</p></th>
<th><p>Valeur</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>HideTheRibbon</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>&lt;CustomUI xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot; &gt; &lt;ruban startFromScratch =&quot;true&quot;/&gt;&lt;/CustomUI&gt;</p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a>Appliquer le ruban personnalisé au démarrage d'Access
=======
<br/>

La table contient les paramètres de personnalisation du ruban à stocker dans la table **RubansSysU**.

|Nom de colonne|Valeur|
|:----------|:----|
|**RibbonName**|HideTheRibbon|
|**RibbonXML**|`<CustomUI xmlns="https://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a>Appliquer un ruban personnalisé au démarrage d’Access
>>>>>>> master

Pour appliquer un ruban personnalisé disponible au démarrage de l'application, procédez comme suit :

1.  Suivez le processus décrit précédemment pour rendre le ruban personnalisé disponible pour cette application.

2.  Redémarrez l'application.

<<<<<<< Tête
3.  Cliquez sur le **Bouton Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") , puis sur **Options Access**.

4.  Cliquez sur l'option **Base de données active**, dans la section **Options de la barre d'outils et du ruban**, puis sur la liste **Nom du ruban** et sélectionnez **HideTheRibbon**.
=======
3.  Cliquez sur le **Bouton Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), puis cliquez sur **Options Access**.

4.  Choisissez l’option de **Base de données actuelle** puis, dans la section **Options de la barre d’outils et du ruban** , cliquez sur la liste **Nom du ruban** et sélectionnez **HideTheRibbon**.
>>>>>>> master

5.  Fermez er redémarrez l'application.

> [!NOTE]
> [!REMARQUE] Pour plus d'informations sur l'interface du ruban dans d'autres applications Office, consultez l'article [Vue d'ensemble du ruban Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


