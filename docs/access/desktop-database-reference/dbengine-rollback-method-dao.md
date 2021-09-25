---
title: DBEngine.Rollback method (DAO)
TOCTitle: Rollback Method
ms:assetid: da7e2fe0-c837-7b1e-d35c-98e6cb0a7bbe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835327(v=office.15)
ms:contentKeyID: 48548084
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053424
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: faac22b235b9ac988cdde5198bc925b25d1a945f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558428"
---
# <a name="dbenginerollback-method-dao"></a>DBEngine.Rollback method (DAO)


**S’applique à** : Access 2013, Office 2013

Met fin à transaction en cours et restaure les bases de données dans l'objet **Workspace** à l'état dans lequel elles se trouvaient au début de la transaction actuelle.

## <a name="syntax"></a>Syntaxe

*.* Rollback

*expression* Variable représentant un objet **DBEngine**.

## <a name="remarks"></a>Remarques

Les méthodes de transaction **BeginTrans**, **CommitTrans** et **Rollback** gèrent le traitement des transactions au cours d'une session définie par un objet **Workspace**. Vous utilisez ces méthodes avec un objet **Workspace** lorsque vous souhaitez traiter une série de modifications apportées en bloc aux bases de données dans une session.

En général, vous utilisez des transactions pour conserver l'intégrité de vos données lorsque vous devez mettre à jour des enregistrements dans deux ou plusieurs tables et vous assurer que les modifications sont terminées (validées) dans toutes les tables ou dans aucune des tables (annulées). Par exemple, si vous transférez de l'argent d'un compte à un autre, vous devez soustraire un montant d'un compte et l'ajouter à un autre compte. Si une de ces mises à jour échoue, les comptes ne sont plus équilibrés. Utilisez la méthode **BeginTrans** avant de mettre à jour le premier enregistrement, puis, si une mise à jour suivante échoue, vous pouvez utiliser la méthode **Rollback** pour annuler toutes les mises à jour. Utilisez la méthode **CommitTrans** une fois que vous avez réussi à mettre à jour le dernier enregistrement.

> [!NOTE]
> [!REMARQUE] Dans un objet **Workspace**, les transactions sont toujours globales dans l'objet **Workspace** et vous n'êtes pas limité à un seul objet **Connection** ou **Database**. Si vous effectuez des opérations sur plusieurs connexions ou bases de données dans une transaction **Workspace**, la résolution de la transaction (à l'aide de la méthode **CommitTrans** ou **Rollback**) affecte toutes les opérations de toutes les connexions et bases de données dans cet espace de travail.

Une fois que vous avez utilisé la méthode **CommitTrans**, vous ne pouvez pas annuler les modifications effectuées au cours de cette transaction sauf si la transaction est imbriquée dans une autre transaction qui est elle-même annulée. Si vous imbriquez des transactions, vous devez résoudre la transaction active avant de pouvoir résoudre une transaction située à un niveau supérieur d'imbrication.

Si vous souhaitez utiliser des transactions simultanées avec des portées non imbriquées qui se chevauchent, vous pouvez créer d'autres objets **Workspace** qui contiennent les transactions concomitantes.

Si vous fermez un objet **Workspace** sans résoudre les transactions en attente, les transactions sont automatiquement annulées.

Si vous utilisez la méthode **CommitTrans** ou **Rollback** sans utiliser d'abord la méthode **BeginTrans**, une erreur se produit.

Certaines bases de données ISAM utilisées dans un espace de travail Microsoft Access peuvent ne pas prendre en charge les transactions, auquel cas la propriété **Transactions** de l'objet **Database** ou **Recordset** prend la valeur **False**. Pour s'assurer que les bases de données prennent en charge les transactions, vérifiez la valeur de la propriété **Transactions** de l'objet **Database** avant d'utiliser la méthode **BeginTrans**. Si vous utilisez un objet **Recordset** basé sur plusieurs bases de données, vérifiez la propriété **Transactions** de l'objet **Recordset**. Si un objet **Recordset** est basé entièrement sur des tables de moteur de base de données Microsoft Access, vous pouvez toujours utiliser des transactions. En revanche, les objets **Recordset** basés sur des tables créées par d'autres produits de base de données ne peuvent pas prendre en charge les transactions. Par exemple, vous ne pouvez pas utiliser de transactions dans un objet **Recordset** basé sur une table Paradox. Dans ce cas, la propriété **Transactions** prend la valeur **False**. Si l'objet **Database** ou **Recordset** ne prend pas en charge les transactions, les méthodes sont ignorées et aucune erreur ne se produit.

Vous ne pouvez pas imbriquer des transactions si vous accédez à des sources de données ODBC par le biais du moteur de base de données Microsoft Access.

Dans les espaces de travail ODBC, lorsque vous utilisez **CommitTrans**, il peut arriver que le curseur ne soit plus valide. Utilisez la méthode **Requery** pour afficher les modifications dans l'objet **Recordset**, ou fermez l'objet **Recordset** et réouvrez-le.

  - Vous pouvez souvent améliorer les performances de l'application en fractionnant les opérations qui doivent accéder au disque en blocs de transactions. Cette opération place les opérations dans la mémoire tampon et peut considérablement réduire le nombre d'accès à un disque.

  - Dans un espace de travail Microsoft Access, les transactions sont journalisées dans un fichier conservé dans le répertoire spécifié par la variable d'environnement TEMP sur le poste de travail. Si le fichier journal des transactions utilise tout l'espace de stockage disponible sur le lecteur TEMP, le moteur de base de données déclenche une erreur d'exécution. À ce niveau, si vous utilisez **CommitTrans**, un nombre indéterminé d'opérations est validé, mais les opérations restantes qui n'ont pas été terminées sont perdues, et l'opération doit être recommencée. L'utilisation de la méthode **Rollback** libère le journal des transactions et annule toutes les opérations dans la transaction.

  - La fermeture d'un objet **Recordset** cloné pendant une transaction en attente entraîne une opération **Rollback** implicite.

