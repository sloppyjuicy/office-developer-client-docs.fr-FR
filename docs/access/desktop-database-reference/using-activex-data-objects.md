---
<<<<<<< Titre tête : à l’aide des TOCTitle d’objets de données ActiveX : ms:assetid à l’aide des objets de données ActiveX : 64055c45-7a27-2296-468a-015362898329 ms:mtpsurl : https://msdn.microsoft.com/library/Ff194969(v=office.15) ms:contentKeyID : ms.date 48545279 : 18/09/2015 === titre : utiliser ActiveX TOCTitle d’objets de données : Description utiliser les objets de données ActiveX : Microsoft Access fournit trois objets modèles à utiliser pour la création, de maintenance et la gestion de vos bases de données Access et leurs données liées à l’aide de Visual Basic.
MS:AssetId : 64055c45-7a27-2296-468a-015362898329 ms:mtpsurl : https://msdn.microsoft.com/library/Ff194969(v=office.15) ms:contentKeyID : ms.date 48545279 : 10/16/2018
>>>>>>> maître mtps_version : v=office.15 f1_keywords :
- vbaac10.chm5285627 f1_categories :
- Office.Version=v15
---

<<<<<<< Tête
# <a name="using-activex-data-objects"></a>Utilisation des objets de données ActiveX


**S’applique à**: Access 2013 | Office 2013

<a name="microsoft-access-provides-three-object-models-to-use-in-the-creation-maintaining-and-managing-of-your-access-databases-and-their-related-data-by-using-visual-basic"></a>Microsoft Access propose trois modèles d'objet à utiliser pour la création, la maintenance et la gestion de vos bases de données Access et de leurs données liées à l'aide de Visual Basic.
=======
# <a name="use-activex-data-objects"></a>Utiliser des objets de données ActiveX

**S’applique à**: Access 2013 | Office 2013

Microsoft Access propose trois modèles d’objet à utiliser pour la création, de maintenance et la gestion de vos bases de données Access et leurs données liées à l’aide de Visual Basic.
>>>>>>> master

## <a name="microsoft-activex-data-objects-ado"></a>Objets de données Microsoft ActiveX (ADO)

ADO contient les objets nécessaires pour créer, maintenir et supprimer des enregistrements dans une source de données.

<<<<<<< Tête
## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO Ext. for DDL and Security (ADOX)

ADOX comprend les objets DDL (Data Definition Language, langage de définition de données) nécessaires pour créer une nouvelle base de données et ses objets contenus en plus des objets nécessaires pour gérer la sécurité.

**Microsoft Jet and Replication Objects 2.5 Library (JRO)**

<a name="since-ado-objects-were-designed-to-work-with-many-databases-in-addition-to-microsoft-jet-databases-functionality-specific-to-jet-was-broken-out-into-the-jro-library"></a>Du fait que les objets ADO ont été créés pour fonctionner avec de nombreuses bases de données, en plus des bases de données Microsoft Jet, la fonctionnalité propre à Jet a été intégrée dans la bibliothèque JRO.
=======
## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO Ext. pour DDL and security (ADOX)

ADOX comprend les objets de langage de définition de données (DDL) nécessaires pour créer une nouvelle base de données et ses objets contenus en plus des objets nécessaires pour gérer la sécurité.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Modèle Microsoft Jet and Replication Objects 2.5 library (JRO)

Étant donné que les objets ADO ont été conçus pour fonctionner avec nombreuses bases de données en plus des bases de données Microsoft Jet, la fonctionnalité propre à Jet a été intégrée dans la bibliothèque JRO.
>>>>>>> master

Le tableau ci-dessous indique les fonctionnalités offertes par chaque composant par rapport à DAO.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fonctionnalités</p></th>
<th><p>DAO</p></th>
<th><p>ADO1</p></th>
<th><p>ADOX2</p></th>
<th><p>JRO<br />
<<<<<<< HEAD (uniquement MDB)</p></th>
=== (MDB uniquement)</p></th>
>>>>>>> master
</tr>
</thead>
<tbody>
<tr class="odd">
<<<<<<< Tête
<td><p>Créer des jeux d’enregistrements</p></td>
=======
<td><p>Créer des jeux d’enregistrements.</p></td>
>>>>>>>forme de base
<td><p>X </p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< Tête
<td><p>Modifier des propriétés de démarrage</p></td>
=======
<td><p>Modifier les propriétés de démarrage.</p></td>
>>>>>>>forme de base
<td><p>X </p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< Tête
<td><p>Prendre en charge ANSI92 SQL***</p></td>
=======
<td><p>Prendre en charge ANSI92 SQL.* **</p></td>
>>>>>>>forme de base
<td><p></p></td>
<td><p>X </p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< Tête
<td><p>Créer des tables</p></td>
=======
<td><p>Créer des tableaux.</p></td>
>>>>>>>forme de base
<td><p>X </p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< Tête
<td><p>Créer une nouvelle base de données</p></td>
=======
<td><p>Créer la nouvelle base de données.</p></td>
>>>>>>>forme de base
<td><p>X </p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< Tête
<td><p>Modifier des propriétés de table existantes</p></td>
=======
<td><p>Modifier les propriétés de table existantes.</p></td>
>>>>>>>forme de base
<td><p>X </p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< Tête
<td><p>Créer des relations de table</p></td>
=======
<td><p>Créer des relations entre les tables.</p></td>
>>>>>>>forme de base
<td><p>X </p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< Tête
<td><p>Modifier des paramètres de sécurité</p></td>
=======
<td><p>Modifier les paramètres de sécurité.</p></td>
>>>>>>>forme de base
<td><p>X </p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< Tête
<td><p>Prendre en charge l’attribut de compression pour les données de colonne</p></td>
=======
<td><p>Prise en charge pour l’attribut de Compression pour les données de colonne.</p></td>
>>>>>>>forme de base
<td><p></p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< Tête
<td><p>Modifier des requêtes ou des vues SQL de base stockées</p></td>
=======
<td><p>Modifier les requêtes SQL ou des vues stockées base.</p></td>
>>>>>>>forme de base
<td><p>X </p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Créer des requêtes permanentes uniquement accessibles par code</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Créer des requêtes accessibles par conteneur/IU et code de base de données</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< Tête
<td><p>Compacter/coder une base de données</p></td>
=======
<td><p>Compacter/coder une base de données.</p></td>
>>>>>>>forme de base
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<<<<<<< Tête
<td><p>Actualiser mémoire cache</p></td>
=======
<td><p>Actualiser le cache.</p></td>
>>>>>>>forme de base
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X </p></td>
</tr>
<tr class="odd">
<<<<<<< Tête
<td><p>Rendre une base de données réplicable</p></td>
=======
<td><p>Rendre la base de données réplicable.</p></td>
>>>>>>>forme de base
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<<<<<<< Tête
<td><p>Faire des réplicas de base de données</p></td>
=======
<td><p>Vérifiez les réplicas de base de données.</p></td>
>>>>>>>forme de base
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<<<<<<< Tête
<td><p>Synchroniser des réplicas</p></td>
=======
<td><p>Synchroniser des réplicas.</p></td>
>>>>>>>forme de base
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<<<<<<< Tête
<td><p>Modifier des propriétés de base de données</p></td>
=======
<td><p>Modifier les propriétés de base de données.</p></td>
>>>>>>>forme de base
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< Tête
<td><p>Créer des propriétés de base de données personnalisées</p></td>
=======
<td><p>Créer des propriétés de base de données personnalisée.</p></td>
>>>>>>>forme de base
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< Tête
<td><p>Modifier les propriétés d’une colonne de table</p></td>
=======
<td><p>Modifier les propriétés de colonne de table.</p></td>
>>>>>>>forme de base
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Uniquement disponible pour la manipulation de bases de données Microsoft Access. Les versions futures de SQL Provider offriront peut-être cette fonctionnalité dans des projets Microsoft Access (.adp).

\*\* Uniquement disponible pour la manipulation de projets Access.

<<<<<<< Tête \* \* \* si le moteur de base de données Access ne prend pas en charge certains codes ANSI 92 SQL n’est pas encore totalement compatible à ANSI92.

1Utilise un objet **Connection** pour faire référence à une base de données

2Utilise un objet **Catalog** pour faire référence à une base de données

3Utilise un objet **Replica** pour faire référence à une base de données

4Utilise un objet **JetEngine** pour faire référence à une base de données


> [!NOTE]
> <a name="punlike-dao-ado-and-adox-objects-can-perform-the-marked-actions-in-databases-other-then-jet-as-long-as-the-provider-for-those-databases-supports-that-actionp"></a><P>[!REMARQUE] À la différence des objets DAO, les objets ADO et ADOX peuvent exécuter les actions indiquées dans des bases de données autres que Jet tant que le fournisseur de celles-ci prend en charge ces actions.</P>
=======
\*\*\*Bien que le moteur de base de données Access ne prend pas en charge certains codes ANSI 92 SQL, il n’est pas encore totalement compatible à ANSI92.

1 objet utilise **connexion** à la base de données de référence.

Objet utilise **catalogue** 2 à la base de données de référence.

Objet 3 utilise **réplica** de base de données de référence.

4 utilise **JetEngine** un objet à la base de données de référence.


> [!NOTE]
> DAO, les objets ADO et ADOX peuvent exécuter les actions indiquées dans les bases de données autres que Jet tant que le fournisseur de celles-ci prend en charge cette action.
>>>>>>> master


