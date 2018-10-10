---
title: Prepared, propriété (ADO)
TOCTitle: Prepared Property (ADO)
ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15)
ms:contentKeyID: 48544116
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231161
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 865453f89cd5942ec7f9f8d036beb72dc519397e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469370"
---
# <a name="prepared-property-ado"></a><span data-ttu-id="3ec4d-102">Prepared, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="3ec4d-102">Prepared Property (ADO)</span></span>


<span data-ttu-id="3ec4d-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ec4d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3ec4d-104">Indique s'il faut enregistrer la version compilée d'une commande avant exécution.</span><span class="sxs-lookup"><span data-stu-id="3ec4d-104">Indicates whether to save a compiled version of a command before execution.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3ec4d-105">Paramètres et valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="3ec4d-105">Settings and Return Values</span></span>

<span data-ttu-id="3ec4d-106">Définit ou renvoie une valeur **booléenne** qui, si elle est définie sur **True**, indique que la commande doit être préparée.</span><span class="sxs-lookup"><span data-stu-id="3ec4d-106">Sets or returns a **Boolean** value that, if set to **True**, indicates that the command should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ec4d-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="3ec4d-107">Remarks</span></span>

<span data-ttu-id="3ec4d-p101">Utilisez la propriété **Prepared** pour que le fournisseur enregistre une version préparée (ou compilée) de la requête spécifiée dans la propriété [CommandText](commandtext-property-ado.md) avant la première exécution d'un objet [Command](command-object-ado.md). Cela risque de ralentir la première exécution de la commande, mais une fois la commande compilée, c'est cette version compilée que le fournisseur utilise lors des exécutions suivantes, ce qui améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="3ec4d-p101">Use the **Prepared** property to have the provider save a prepared (or compiled) version of the query specified in the [CommandText](commandtext-property-ado.md) property before a [Command](command-object-ado.md) object's first execution. This may slow a command's first execution, but once the provider compiles a command, the provider will use the compiled version of the command for any subsequent executions, which will result in improved performance.</span></span>

<span data-ttu-id="3ec4d-110">Si la valeur de la propriété est **False**, le fournisseur exécute l'objet **Command** directement sans créer de version compilée.</span><span class="sxs-lookup"><span data-stu-id="3ec4d-110">If the property is **False**, the provider will execute the **Command** object directly without creating a compiled version.</span></span>

<span data-ttu-id="3ec4d-p102">Si le fournisseur ne prend pas en charge la préparation des commandes, il peut renvoyer une erreur dès que la valeur **True** est attribuée à cette propriété. S'il ne renvoie pas d'erreur, il ignore simplement la requête de préparation et attribue la valeur **False** à la propriété **Prepared**.</span><span class="sxs-lookup"><span data-stu-id="3ec4d-p102">If the provider does not support command preparation, it may return an error as soon as this property is set to **True**. If it does not return an error, it simply ignores the request to prepare the command and sets the **Prepared** property to **False**.</span></span>

