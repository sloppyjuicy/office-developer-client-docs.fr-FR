---
title: MarshalOptions, propriété (ADO)
TOCTitle: MarshalOptions Property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f290f2f4fb4820fb01d3a63aef7bcfbfa7c1f035
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471636"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="b8bfa-102">MarshalOptions, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="b8bfa-102">MarshalOptions Property (ADO)</span></span>


<span data-ttu-id="b8bfa-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8bfa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b8bfa-104">Indique les enregistrements dont les paramètres doivent être convertis avant d'être renvoyés vers le serveur.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b8bfa-105">Paramètres et valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="b8bfa-105">Settings And Return Values</span></span>

<span data-ttu-id="b8bfa-p101">Définit ou renvoie une valeur [MarshalOptions](marshaloptionsenum.md). La valeur par défaut est **adMarshalAll**.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-p101">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value. The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8bfa-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="b8bfa-108">Remarks</span></span>

<span data-ttu-id="b8bfa-p102">Lorsque l'on utilise un [Recordset](recordset-object-ado.md) côté client, les enregistrements modifiés sur le client sont réécrits sur le niveau intermédiaire ou le serveur Web via une technique appelée marshaling ou conversion de paramètres (processus d'empaquetage et d'envoi des paramètres des méthodes de l'interface au-delà des limites des threads ou des processus). La définition de la propriété **MarshalOptions** peut améliorer les performances lorsque les paramètres des données distantes modifiées sont convertis pour être mis à jour sur le niveau intermédiaire ou le serveur Web.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-p102">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or Web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries. Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or Web server.</span></span>

<span data-ttu-id="b8bfa-111">**L’utilisation du Service de données à distance** Cette propriété est utilisée uniquement sur un **jeu d’enregistrements**du côté client.</span><span class="sxs-lookup"><span data-stu-id="b8bfa-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

