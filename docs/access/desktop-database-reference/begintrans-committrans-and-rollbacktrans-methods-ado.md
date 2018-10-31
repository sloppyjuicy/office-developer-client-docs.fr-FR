---
title: BeginTrans, CommitTrans et RollbackTrans, méthodes (ADO)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans Methods (ADO)
ms:assetid: 9a0415f0-9424-8d1c-4779-92e932292d46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249694(v=office.15)
ms:contentKeyID: 48546529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 719c495e18fb769a2d3f994542ab8d9e93a469f1
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860377"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a>BeginTrans, CommitTrans et RollbackTrans, méthodes (ADO)


**S’applique à**: Access 2013 | Office 2013


Ces méthodes de transaction gèrent le traitement des transactions dans un objet [Connection](connection-object-ado.md) de la façon suivante :

  - **BeginTrans**: lance une nouvelle transaction.

  - **CommitTrans**: enregistre les modifications apportées et termine la transaction active. Lance aussi parfois une nouvelle transaction.

  - **RollbackTrans**: annule les modifications apportées pendant la transaction active et termine celle-ci. Lance aussi parfois une nouvelle transaction.

## <a name="syntax"></a>Syntaxe

*niveau* = *objet*. BeginTrans()

*objet*. BeginTrans

*objet*. CommitTrans

*objet*. RollbackTrans

<<<<<<< EN-TÊTE
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

**BeginTrans** peut être appelée en tant que fonction qui retourne une variable de type **Long** indiquant le niveau d'imbrication de la transaction.

## <a name="parameters"></a>Paramètres

  - *object*

  - Objet **Connection**.

**Connection**

Utilisez ces méthodes avec un objet **Connection** lorsque vous voulez enregistrer ou annuler en bloc une série de modifications apportées aux données source. Par exemple, pour transférer de l'argent entre des comptes, vous soustrayez le montant transféré d'un compte et vous ajoutez ce même montant à l'autre compte. Si l'opération échoue d'un côté, les comptes ne seront plus équilibrés. Lorsque vous effectuez des modifications de ce type dans une transaction ouverte, vous êtes assuré que toutes les modifications ou aucune d'elles sont validées.


> [!NOTE]
> Tous les fournisseurs ne prennent pas en charge les transactions. Vérifiez que la propriété « **Transaction DDL** », définie par le fournisseur, apparaît dans la collection [Properties](properties-collection-ado.md) de l’objet **Connection** ; elle indique que le fournisseur prend en charge les transactions. Si ce n’est pas le cas, l’appel de l’une de ces méthodes retourne une erreur.

Une fois que vous appelez la méthode **BeginTrans**, le fournisseur ne valide plus instantanément les modifications que vous apportez jusqu'à ce que vous appeliez **CommitTrans** ou **RollbackTrans** pour mettre fin à la transaction.

Pour les fournisseurs qui prennent en charge les transactions imbriquées, l'appel de la méthode **BeginTrans** dans une transaction ouverte lance une nouvelle transaction imbriquée. La valeur de retour indique le niveau d'imbrication ; ainsi, la valeur 1 indique que vous avez ouvert une transaction de niveau supérieur (la transaction n'est pas imbriquée dans une autre), la valeur 2 que vous avez ouvert une transaction de deuxième niveau (une transaction imbriquée dans une transaction de niveau supérieur), etc. L'appel de la méthode **CommitTrans** ou **RollbackTrans** n'affecte que les dernières transactions ouvertes ; vous devez fermer ou annuler la transaction active pour pouvoir résoudre des transactions de niveau supérieur.

L'appel de la méthode **CommitTrans** enregistre les modifications apportées dans une transaction ouverte sur la connexion et clôture la transaction. La méthode **RollbackTrans**, quant à elle, annule les modifications apportées dans une transaction ouverte et met fin à la transaction. Si aucune transaction n'est ouverte, l'appel de ces méthodes génère une erreur.

En fonction de la propriété [Attributes](attributes-property-ado.md) de l’objet **Connection** , l’appel de la méthode **CommitTrans** ou **RollbackTrans** peut démarrer automatiquement une nouvelle transaction. Si la propriété **Attributes** a la valeur **adXactCommitRetaining**, le fournisseur lance automatiquement une nouvelle transaction après un appel à **CommitTrans**. Si la propriété **Attributes** a la valeur **adXactAbortRetaining**, le fournisseur lance automatiquement une nouvelle transaction après un appel à **RollbackTrans**.

**RDS (Remote Data Service)**

Les méthodes **BeginTrans**, **CommitTrans** et **RollbackTrans** ne sont pas disponibles sur un objet **Connection** côté client.

