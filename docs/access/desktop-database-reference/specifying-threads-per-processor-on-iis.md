---
title: Définition du nombre de threads par processeur dans IIS
TOCTitle: Specifying Threads Per Processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de3c8c99c7f615928ea0a0f1e15171cc90b25f3d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469672"
---
# <a name="specifying-threads-per-processor-on-iis"></a><span data-ttu-id="07f11-102">Définition du nombre de threads par processeur dans IIS</span><span class="sxs-lookup"><span data-stu-id="07f11-102">Specifying Threads Per Processor on IIS</span></span>


<span data-ttu-id="07f11-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="07f11-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="07f11-p101">Lorsque vous utilisez RDS avec Internet Information Services 4.0 ou une version ultérieure, le nombre de threads créés par processeur peut être contrôlé en manipulant le Registre du serveur Web. Le nombre de threads par processeur peut avoir des répercussions négatives sur les performances en cas de trafic élevé ou lorsque le trafic est faible mais que les requêtes sont complexes et volumineuses. L'utilisateur est invité à tenter des expériences pour obtenir les meilleurs résultats possibles.</span><span class="sxs-lookup"><span data-stu-id="07f11-p101">When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the Web server. The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes. The user should experiment for best results.</span></span>

<span data-ttu-id="07f11-107">La méthode utilisée pour déterminer et modifier la valeur par défaut de ce paramètre dépend de la configuration du serveur IIS 4.0.</span><span class="sxs-lookup"><span data-stu-id="07f11-107">The method used to determine and change the default value for this setting depends upon the configuration of the IIS 4.0 server.</span></span>

<span data-ttu-id="07f11-p102">Dans la mesure où MDAC 2.1.2.4202.3 (GA) ou une version ultérieure est installé sur le serveur IIS, RDS utilise le même pool de threads des services de composants (ou de Microsoft Transaction Services, si vous utilisez Windows NT) que les scripts ASP. Par défaut, le nombre de threads par processeur est de 10. Pour modifier cette valeur par défaut, vous devez ajouter la clé suivante au Registre du serveur :</span><span class="sxs-lookup"><span data-stu-id="07f11-p102">With MDAC 2.1.2.4202.3 (GA) or later installed on the IIS server, RDS uses the same Component Services (or Microsoft Transaction Services, if you are using Windows NT) thread pool as ASP scripts use. The default value for the number of threads per processor is 10. To change the default, you must add the following key to the server registry:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

<span data-ttu-id="07f11-111">*MaxPoolThreads* correspond à un Registre\_DWORD.</span><span class="sxs-lookup"><span data-stu-id="07f11-111">where *MaxPoolThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="07f11-112">*MaxPoolThreads* n’apparaît pas dans le Registre, sauf si elle est ajoutée en particulier.</span><span class="sxs-lookup"><span data-stu-id="07f11-112">*MaxPoolThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="07f11-113">Les valeurs valides s'échelonnent de 5 à une valeur maximale recommandée de 20.</span><span class="sxs-lookup"><span data-stu-id="07f11-113">Valid values range from 5 to a recommended maximum of 20.</span></span> <span data-ttu-id="07f11-114">Si la valeur spécifiée par la clé de Registre est supérieure à la valeur de la clé *PoolThreadLimit* (située sous le même chemin d’accès), la valeur de *PoolThreadLimit* est utilisée.</span><span class="sxs-lookup"><span data-stu-id="07f11-114">If the value specified by the registry key is greater than the value of the *PoolThreadLimit* key (located under the same path), then *PoolThreadLimit* value is used.</span></span>

<span data-ttu-id="07f11-p104">Sinon, si MDAC 2.1 2.1.1.3711.11 (GA) ou une version antérieure est installé sur le serveur IIS, le nombre de threads par processeur est de 6, par défaut. Pour modifier cette valeur par défaut, vous devez ajouter la clé suivante au Registre du serveur IIS :</span><span class="sxs-lookup"><span data-stu-id="07f11-p104">Alternatively, if MDAC 2.1 2.1.1.3711.11 (GA) or earlier is installed on the IIS server, the default value for the number of threads per processor is 6. To change the default, you must add the following key to the registry on the IIS server:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

<span data-ttu-id="07f11-117">*ADCThreads* correspond à un Registre\_DWORD.</span><span class="sxs-lookup"><span data-stu-id="07f11-117">where *ADCThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="07f11-118">*ADCThreads* n’apparaît pas dans le Registre, sauf si elle est ajoutée en particulier.</span><span class="sxs-lookup"><span data-stu-id="07f11-118">*ADCThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="07f11-119">Les valeurs valides s'échelonnent de 1 à 50.</span><span class="sxs-lookup"><span data-stu-id="07f11-119">The range of valid values is 1 to 50.</span></span> <span data-ttu-id="07f11-120">Si la valeur spécifiée par la clé de Registre est supérieure à 50, la valeur maximale est utilisée (50).</span><span class="sxs-lookup"><span data-stu-id="07f11-120">If the value specified by the registry key is greater than 50, then the maximum value is used (50).</span></span>

