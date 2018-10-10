---
title: Connection.Execute Method (DAO)
TOCTitle: Execute Method
ms:assetid: d6140d4e-fa14-6455-525e-49d8aab3dff7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835040(v=office.15)
ms:contentKeyID: 48547978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3171ec1d35f08a5bc9d6a02a9a50ca80e11413de
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471477"
---
# <a name="connectionexecute-method-dao"></a>Connection.Execute Method (DAO)


**S’applique à**: Access 2013 | Office 2013

Exécute une requête Action ou une instruction SQL sur l'objet spécifié.

## <a name="syntax"></a>Syntaxe

*expression* . Execute (***requête***, ***Options***)

*expression* Variable qui représente un objet **Connection** .

### <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Obligatoire/Facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Query</p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Chaîne</strong></p></td>
<td><p>Type <strong>String</strong> qui représente une instruction SQL ou la valeur de la propriété <strong>Name</strong> d'un objet <strong>QueryDef</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Options</p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p>Constante ou combinaison de constantes déterminant les caractéristiques d'intégrité des données de la requêtes, comme indiqué dans la section Remarques.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez utiliser l’une des constantes **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** suivantes pour les options.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDenyWrite</strong></p></td>
<td><p>Refuse les autorisations d'accès en écriture aux autres utilisateurs (espaces de travail Microsoft Access uniquement)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInconsistent</strong></p></td>
<td><p>(Option par défaut) Exécute les mises à jour incohérentes (espaces de travail Microsoft Access uniquement)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbConsistent</strong></p></td>
<td><p>Exécute les mises à jour cohérentes (espaces de travail Microsoft Access uniquement)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSQLPassThrough</strong></p></td>
<td><p>Exécute une requête SQL directe. Si elle est définie, cette option transmet l'instruction SQL à une base de données ODBC pour traitement (espaces de travail Microsoft Access uniquement)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFailOnError</strong></p></td>
<td><p>Annule les mises à jour si une erreur se produit (espaces de travail Microsoft Access uniquement)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSeeChanges</strong></p></td>
<td><p>Génère une erreur d'exécution si un autre utilisateur modifie les données que vous-même êtes en train de modifier (espaces de travail Microsoft Access uniquement)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Exécute la requête en mode asynchrone (objets ODBCDirect Connection et QueryDef uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbExecDirect</strong></p></td>
<td><p>Exécute l'instruction sans appeler préalablement la fonction API ODBC SQLPrepare (objets ODBCDirect Connection et QueryDef uniquement).</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</P>




> [!NOTE]
> <P>[!REMARQUE] Les constantes <STRONG>dbConsistent</STRONG> et <STRONG>dbInconsistent</STRONG> s'excluent mutuellement. Vous pouvez utiliser l'une ou l'autre, mais jamais les deux en même temps dans une instance donnée d' <STRONG>OpenRecordset</STRONG>. L'utilisation de <STRONG>dbConsistent</STRONG> et <STRONG>dbInconsistent</STRONG> génère une erreur.</P>



La méthode **Execute** est valide uniquement pour les requêtes action. Si vous utilisez **Execute** avec un autre type de requête, une erreur est générée. Dans la mesure où une requête Action ne renvoie aucun enregistrement, **Execute** ne renvoie pas d'objet **Recordset**. (L'exécution d'une requête SQL directe dans un espace de travail ODBCDirect ne renvoie pas d'erreur si aucun objet **Recordset** n'est renvoyé.)

Utilisez la propriété **RecordsAffected** de l'objet **Connection**, **Database** ou **QueryDef** pour déterminer le nombre d'enregistrements affectés par le dernier appel de la méthode **Execute**. **RecordsAffected** contient, par exemple, le nombre d'enregistrements supprimés, mis à jour ou insérés lors de l'exécution d'une requête Action. Lorsque vous utilisez la méthode **Execute** pour exécuter une requête, la propriété **RecordsAffected** de l'objet **QueryDef** a pour valeur le nombre d'enregistrements affectés.

Dans un espace de travail Microsoft Access, si vous fournissez une instruction SQL avec une syntaxe correcte et disposez des autorisations appropriées, la méthode **Execute** n'échoue pas même si aucune ligne n'a pu être modifiée ou supprimée. Par conséquent, utilisez toujours l'option **dbFailOnError** avec la méthode **Execute** pour exécuter une requête Suppression ou Mise à jour. Cette option génère une erreur d'exécution et annule toutes les modifications implémentées si l'un des enregistrements affectés est verrouillé et ne peut être mis à jour, ni supprimé.

Dans les versions antérieures du moteur de base de données Microsoft Jet, les instructions SQL étaient automatiquement incorporées dans des transactions implicites. Si une partie d'une instruction exécutée avec **dbFailOnError** échouait, toute l'instruction était annulée. Pour améliorer les performances, ces transactions implicites ont été supprimées à partir de la version 3.5. Si vous mettez à jour un code DAO plus ancien, envisagez d'utiliser des transactions explicites avec les instructions **Execute**.

Pour obtenir de meilleures performances dans un espace de travail Microsoft Access, en particulier dans un environnement multi-utilisateur, imbriquez la méthode **Execute** dans une transaction. Utilisez la méthode **BeginTrans** sur l'objet **Workspace** actif puis utilisez la méthode **Execute** et terminez la transaction en appelant la méthode **CommitTrans** sur l'objet **Workspace**. Cette opération permet d'enregistrer les modifications sur disque et de libérer tous les verrous appliqués pendant l'exécution de la requête.

