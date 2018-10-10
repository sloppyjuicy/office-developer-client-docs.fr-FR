---
title: 'Chapitre 7 : Gestion des événements ADO'
TOCTitle: 'Chapter 7: Handling ADO Events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d85532c93c6d175b90f957d7831b71a460ba5b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471751"
---
# <a name="chapter-7-handling-ado-events"></a><span data-ttu-id="dd69e-102">Chapitre 7 : Gestion des événements ADO</span><span class="sxs-lookup"><span data-stu-id="dd69e-102">Chapter 7: Handling ADO Events</span></span>


<span data-ttu-id="dd69e-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd69e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dd69e-p101">Le modèle d’événements ADO prend en charge certaines opérations synchrones et asynchrones, qui génèrent des *événements*, ou notifications, avant et après leur exécution. Un événement représente, en fait, l’appel d’une routine de gestionnaire d’événements que vous définissez dans votre application.</span><span class="sxs-lookup"><span data-stu-id="dd69e-p101">The ADO event model supports certain synchronous and asynchronous ADO operations that issue *events*, or notifications, before the operation starts or after it completes. An event is actually a call to an event-handler routine that you define in your application.</span></span>

<span data-ttu-id="dd69e-p102">Si vous fournissez des fonctions ou des procédures de gestionnaire pour les événements qui se produisent avant l'exécution de l'opération, vous pouvez examiner ou modifier les paramètres qui ont été transmis à celle-ci. En outre, étant donné que l'opération n'a pas encore été exécutée, vous pouvez l'annuler ou lui permettre d'aller à son terme.</span><span class="sxs-lookup"><span data-stu-id="dd69e-p102">If you provide handler functions or procedures for the group of events that occur before the operation starts, you can examine or modify the parameters that were passed to the operation. Because it has not been executed yet, you can either cancel the operation or allow it to complete.</span></span>

<span data-ttu-id="dd69e-p103">Les événements qui se produisent au terme d'une opération sont particulièrement importants si vous utilisez ADO de façon asynchrone. Par exemple, une application qui lance une opération [Recordset.Open](open-method-ado-recordset.md) asynchrone est avertie de la fin de l'opération par un événement de fin d'exécution.</span><span class="sxs-lookup"><span data-stu-id="dd69e-p103">The group of events that occur after an operation completes are especially important if you use ADO asynchronously. For example, an application that starts an asynchronous [Recordset.Open](open-method-ado-recordset.md) operation is notified by an execution complete event when the operation concludes.</span></span>

<span data-ttu-id="dd69e-110">L'utilisation du modèle d'événements ADO, bien qu'elle constitue une surcharge pour votre application, offre plus de souplesse que les autres méthodes de traitement des opérations asynchrones, telles que le contrôle de la propriété [State](state-property-ado.md) d'un objet avec une boucle.</span><span class="sxs-lookup"><span data-stu-id="dd69e-110">Using the ADO event model adds some overhead to your application but provides far more flexibility than other methods of dealing with asynchronous operations, such as monitoring the [State](state-property-ado.md) property of an object with a loop.</span></span>

