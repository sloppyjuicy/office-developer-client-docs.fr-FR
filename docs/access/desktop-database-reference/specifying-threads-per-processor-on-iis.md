---
title: Spécification de threads par processeur sur IIS
TOCTitle: Specifying threads per processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 57e4b6228588af7f0d58caf53d3e093e824c7854
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308588"
---
# <a name="specifying-threads-per-processor-on-iis"></a>Spécification de threads par processeur sur IIS


**S’applique à** : Access 2013, Office 2013

Lorsque vous utilisez RDS avec Internet Information Services 4.0 ou une ultérieure, le nombre de threads créés par processeur peut être contrôlé en manipulant le Registre sur le serveur web. Le nombre de threads par processeur peut avoir des répercussions négatives sur les performances en cas de trafic élevé ou lorsque le trafic est faible mais que les requêtes sont complexes et volumineuses. L'utilisateur est invité à tenter des expériences pour obtenir les meilleurs résultats possibles.

La méthode utilisée pour déterminer et modifier la valeur par défaut de ce paramètre dépend de la configuration du serveur IIS 4.0.

Dans la mesure où MDAC 2.1.2.4202.3 (GA) ou une version ultérieure est installé sur le serveur IIS, RDS utilise le même pool de threads des services de composants (ou de Microsoft Transaction Services, si vous utilisez Windows NT) que les scripts ASP. Par défaut, le nombre de threads par processeur est de 10. Pour modifier cette valeur par défaut, vous devez ajouter la clé suivante au Registre du serveur :

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

où *MaxPoolThreads est* un \_ REG DWORD. La clé *MaxPoolThreads* n'apparaît pas dans le Registre à moins qu'elle ait été spécialement ajoutée. Les valeurs valides s'échelonnent de 5 à une valeur maximale recommandée de 20. Si la valeur spécifiée par la clé de Registre est supérieure à la valeur de la clé *PoolThreadLimit* (située dans le même chemin), la valeur de *PoolThreadLimit* est utilisée.

Sinon, si MDAC 2.1 2.1.1.3711.11 (GA) ou une version antérieure est installé sur le serveur IIS, le nombre de threads par processeur est de 6, par défaut. Pour modifier cette valeur par défaut, vous devez ajouter la clé suivante au Registre du serveur IIS :

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

où *ADCThreads est* un REG \_ DWORD. La clé *ADCThreads* n'apparaît pas dans le Registre à moins qu'elle ait été spécialement ajoutée. Les valeurs valides s'échelonnent de 1 à 50. Si la valeur spécifiée par la clé de Registre est supérieure à 50, la valeur maximale est utilisée (50).

