---
title: Définition d'un verrou (Référence de base de données de bureau Access)
TOCTitle: What is a Lock?
ms:assetid: 9ddc3198-1531-1d8f-153d-fc79847e388a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249721(v=office.15)
ms:contentKeyID: 48546636
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5e503fd15d9864cc6ab007de031493e321622246
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306761"
---
# <a name="what-is-a-lock"></a><span data-ttu-id="be577-103">Qu’est-ce qu’un verrou ?</span><span class="sxs-lookup"><span data-stu-id="be577-103">What is a lock?</span></span>


<span data-ttu-id="be577-104">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be577-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be577-p102">Le verrouillage est le processus par lequel un SGBD limite l'accès à une ligne dans un environnement multi-utilisateur. Lorsqu'une ligne ou une colonne est verrouillée en mode exclusif, les autres utilisateurs ne sont pas autorisés à accéder aux données avant que le verrou soit libéré. Il s'agit d'une procédure de sécurité qui permet d'éviter la mise à jour simultanée de la même colonne d'une ligne par deux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="be577-p102">Locking is the process by which a DBMS restricts access to a row in a multi-user environment. When a row or column is exclusively locked, other users are not permitted to access the locked data until the lock is released. This ensures that two users cannot simultaneously update the same column in a row.</span></span>

<span data-ttu-id="be577-p103">Les verrous peuvent s'avérer très coûteux en termes de ressources. Il est donc conseillé de les utiliser dans le seul cas où il est impératif de préserver l'intégrité des données. Dans une base de données où des centaines, voire des milliers d'utilisateurs, sont susceptibles d'accéder aux enregistrements à chaque seconde, par exemple une base de données connectée à Internet, un verrouillage superflu peut rapidement engendrer un ralentissement des performances de l'application.</span><span class="sxs-lookup"><span data-stu-id="be577-p103">Locks can be very expensive from a resource perspective and should be used only when required to preserve data integrity. In a database where hundreds or thousands of users could be trying to access a record every second — such as a database connected to the Internet — unnecessary locking could quickly result in slower performance in your application.</span></span>

<span data-ttu-id="be577-110">Vous pouvez contrôler la façon dont la source de données et la bibliothèque de curseurs ADO gèrent l'accès concurrentiel en choisissant l'option de verrouillage appropriée.</span><span class="sxs-lookup"><span data-stu-id="be577-110">You can control how the data source and the ADO cursor library manage concurrency by choosing the appropriate locking option.</span></span>

<span data-ttu-id="be577-p104">Définissez la propriété **LockType** avant d'ouvrir un objet **Recordset** pour spécifier le type de verrouillage que le fournisseur doit utiliser pour son ouverture. Lisez la propriété pour obtenir le type de verrouillage actuellement utilisé sur un objet **Recordset** ouvert.</span><span class="sxs-lookup"><span data-stu-id="be577-p104">Set the **LockType** property before opening a **Recordset** to specify what type of locking the provider should use when opening it. Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="be577-p105">Certains fournisseurs ne prennent pas tous les types de verrou en charge. Si un fournisseur ne prend pas en charge le paramètre **LockType** requis, il lui substituera automatiquement un autre type de verrou. Utilisez la méthode **Supports** avec [adUpdate](supports-method-ado.md) et **adUpdateBatch** pour déterminer les fonctionnalités de verrouillage disponibles dans un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="be577-p105">Providers might not support all lock types. If a provider cannot support the requested **LockType** setting, it will substitute another type of locking. To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="be577-p106">Le paramètre **adLockPessimistic** n'est pas pris en charge si la propriété [CursorLocation](cursorlocation-property-ado.md) a la valeur **adUseClient**. Si vous définissez une valeur non prise en charge, aucune erreur n'est générée ; elle sera simplement remplacée par la valeur de **LockType** la plus similaire prise en charge.</span><span class="sxs-lookup"><span data-stu-id="be577-p106">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="be577-118">La propriété **LockType** est accessible en lecture/écriture lorsque l'objet **Recordset** est fermé, et en lecture seule lorsqu'il est ouvert.</span><span class="sxs-lookup"><span data-stu-id="be577-118">The **LockType** property is read/write when the **Recordset** is closed, and read-only when it is open.</span></span>

<span data-ttu-id="be577-119">Cette section comprend les rubriques suivantes:</span><span class="sxs-lookup"><span data-stu-id="be577-119">This section includes the following topic:</span></span>

- [<span data-ttu-id="be577-120">Types de verrous</span><span class="sxs-lookup"><span data-stu-id="be577-120">Types of Locks</span></span>](types-of-locks.md)

