---
title: DBEngine.CommitTrans Method (DAO)
TOCTitle: CommitTrans Method
ms:assetid: 0c9d345f-13ff-7fe6-789d-fbdb43fa54b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845171(v=office.15)
ms:contentKeyID: 48543197
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3306c81af03b374416c948f44107690f188769cc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472320"
---
# <a name="dbenginecommittrans-method-dao"></a>DBEngine.CommitTrans Method (DAO)


**S’applique à**: Access 2013 | Office 2013

Met fin à la transaction en cours et enregistre les modifications.

## <a name="syntax"></a>Syntaxe

*expression* . CommitTrans (***Option***)

*expression* Variable qui représente un objet **DBEngine** .

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
<td><p>Option</p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Entier long</strong></p></td>
<td><p>Dans un espace de travail Microsoft Access, vous pouvez inclure la constante <strong>dbForceOSFlush</strong> avec <strong>CommitTrans</strong>. Cela force le moteur de base de données à purger toutes les mises à jour sur le disque au lieu de les mettre en mémoire cache temporairement. Sans cette option, un utilisateur peut reprendre le contrôle dès que le programme d’application appelle <strong>CommitTrans</strong>, éteindre l’ordinateur et les données ne sont pas écrites sur le disque. Même si cette option peut affecter les performances de votre application, elle s’avère utile dans les situations dans lesquelles l’ordinateur a pu être fermé avant que les mises à jour mises en mémoire cache ne soient enregistrées sur le disque.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Les méthodes de transaction **BeginTrans**, **CommitTrans** et **Rollback** gèrent le traitement des transactions au cours d'une session définie par un objet **Workspace**. Vous utilisez ces méthodes avec un objet **Workspace** lorsque vous souhaitez traiter une série de modifications apportées en bloc aux bases de données dans une session.

En général, vous utilisez des transactions pour conserver l'intégrité de vos données lorsque vous devez mettre à jour des enregistrements dans deux ou plusieurs tables et vous assurer que les modifications sont terminées (validées) dans toutes les tables ou dans aucune des tables (annulées). Par exemple, si vous transférez de l'argent d'un compte à un autre, vous devez soustraire un montant d'un compte et l'ajouter à un autre compte. Si une de ces mises à jour échoue, les comptes ne sont plus équilibrés. Utilisez la méthode **BeginTrans** avant de mettre à jour le premier enregistrement, puis, si une mise à jour suivante échoue, vous pouvez utiliser la méthode **Rollback** pour annuler toutes les mises à jour. Utilisez la méthode **CommitTrans** une fois que vous avez réussi à mettre à jour le dernier enregistrement.


> [!NOTE]
> <P>[!REMARQUE] Dans un objet <STRONG>Workspace</STRONG>, les transactions sont toujours globales dans l'objet <STRONG>Workspace</STRONG> et vous n'êtes pas limité à un seul objet <STRONG>Connection</STRONG> ou <STRONG>Database</STRONG>. Si vous effectuez des opérations sur plusieurs connexions ou bases de données dans une transaction <STRONG>Workspace</STRONG>, la résolution de la transaction (à l'aide de la méthode <STRONG>CommitTrans</STRONG> ou <STRONG>Rollback</STRONG>) affecte toutes les opérations de toutes les connexions et bases de données dans cet espace de travail.</P>



Une fois que vous avez utilisé la méthode **CommitTrans**, vous ne pouvez pas annuler les modifications effectuées au cours de cette transaction sauf si la transaction est imbriquée dans une autre transaction qui est elle-même annulée. Si vous imbriquez des transactions, vous devez résoudre la transaction active avant de pouvoir résoudre une transaction située à un niveau supérieur d'imbrication.

Si vous souhaitez utiliser des transactions simultanées avec des portées non imbriquées qui se chevauchent, vous pouvez créer d'autres objets **Workspace** qui contiennent les transactions concomitantes.

Si vous fermez un objet **Workspace** sans résoudre les transactions en attente, les transactions sont automatiquement annulées.

Si vous utilisez la méthode **CommitTrans** ou **Rollback** sans utiliser d'abord la méthode **BeginTrans**, une erreur se produit.

Certaines bases de données ISAM utilisées dans un espace de travail Microsoft Access peuvent ne pas prendre en charge les transactions, auquel cas la propriété **Transactions** de l'objet **Database** ou **Recordset** prend la valeur **False**. Pour s'assurer que les bases de données prennent en charge les transactions, vérifiez la valeur de la propriété **Transactions** de l'objet **Database** avant d'utiliser la méthode **BeginTrans**. Si vous utilisez un objet **Recordset** basé sur plusieurs bases de données, vérifiez la propriété **Transactions** de l'objet **Recordset**. Si un objet **Recordset** est basé entièrement sur des tables de moteur de base de données Microsoft Access, vous pouvez toujours utiliser des transactions. En revanche, les objets **Recordset** basés sur des tables créées par d'autres produits de base de données ne peuvent pas prendre en charge les transactions. Par exemple, vous ne pouvez pas utiliser de transactions dans un objet **Recordset** basé sur une table Paradox. Dans ce cas, la propriété **Transactions** prend la valeur **False**. Si l'objet **Database** ou **Recordset** ne prend pas en charge les transactions, les méthodes sont ignorées et aucune erreur ne se produit.

Vous ne pouvez pas imbriquer des transactions si vous accédez à des sources de données ODBC par le biais du moteur de base de données Microsoft Access.

Dans les espaces de travail ODBC, lorsque vous utilisez **CommitTrans**, il peut arriver que le curseur ne soit plus valide. Utilisez la méthode **Requery** pour afficher les modifications dans l'objet **Recordset**, ou fermez l'objet **Recordset** et réouvrez-le.


> [!NOTE]
> <UL>
> <LI>
> <P>Vous pouvez souvent améliorer les performances de l'application en fractionnant les opérations qui doivent accéder au disque en blocs de transactions. Cette opération place les opérations dans la mémoire tampon et peut considérablement réduire le nombre d'accès à un disque.</P>
> <LI>
> <P>Dans un espace de travail Microsoft Access, les transactions sont journalisées dans un fichier conservé dans le répertoire spécifié par la variable d'environnement TEMP sur le poste de travail. Si le fichier journal des transactions utilise tout l'espace de stockage disponible sur le lecteur TEMP, le moteur de base de données déclenche une erreur d'exécution. À ce niveau, si vous utilisez <STRONG>CommitTrans</STRONG>, un nombre indéterminé d'opérations est validé, mais les opérations restantes qui n'ont pas été terminées sont perdues, et l'opération doit être recommencée. L'utilisation de la méthode <STRONG>Rollback</STRONG> libère le journal des transactions et annule toutes les opérations dans la transaction.</P>
> <LI>
> <P>La fermeture d'un objet <STRONG>Recordset</STRONG> cloné pendant une transaction en attente entraîne une opération <STRONG>Rollback</STRONG> implicite.</P></LI></UL>


