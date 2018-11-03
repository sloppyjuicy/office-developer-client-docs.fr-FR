---
title: Spécification des threads par processeur dans IIS
TOCTitle: Specifying threads per processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 78d4ad5b2cf87f390051793b290e174fc03e6a82
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947195"
---
# <a name="specifying-threads-per-processor-on-iis"></a>Spécification des threads par processeur dans IIS


**S’applique à**: Access 2013, Office 2013

Lors de l’utilisation de RDS avec Internet Information Services 4.0 ou version ultérieure, le nombre de threads créés par processeur peut être contrôlé par manipulation du Registre sur le serveur web. Le nombre de threads par processeur peut avoir des répercussions négatives sur les performances en cas de trafic élevé ou lorsque le trafic est faible mais que les requêtes sont complexes et volumineuses. L'utilisateur est invité à tenter des expériences pour obtenir les meilleurs résultats possibles.

La méthode utilisée pour déterminer et modifier la valeur par défaut de ce paramètre dépend de la configuration du serveur IIS 4.0.

Dans la mesure où MDAC 2.1.2.4202.3 (GA) ou une version ultérieure est installé sur le serveur IIS, RDS utilise le même pool de threads des services de composants (ou de Microsoft Transaction Services, si vous utilisez Windows NT) que les scripts ASP. Par défaut, le nombre de threads par processeur est de 10. Pour modifier cette valeur par défaut, vous devez ajouter la clé suivante au Registre du serveur :

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

*MaxPoolThreads* correspond à un Registre\_DWORD. *MaxPoolThreads* n’apparaît pas dans le Registre, sauf si elle est ajoutée en particulier. Les valeurs valides s'échelonnent de 5 à une valeur maximale recommandée de 20. Si la valeur spécifiée par la clé de Registre est supérieure à la valeur de la clé *PoolThreadLimit* (située sous le même chemin d’accès), la valeur de *PoolThreadLimit* est utilisée.

Sinon, si MDAC 2.1 2.1.1.3711.11 (GA) ou une version antérieure est installé sur le serveur IIS, le nombre de threads par processeur est de 6, par défaut. Pour modifier cette valeur par défaut, vous devez ajouter la clé suivante au Registre du serveur IIS :

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

*ADCThreads* correspond à un Registre\_DWORD. *ADCThreads* n’apparaît pas dans le Registre, sauf si elle est ajoutée en particulier. Les valeurs valides s'échelonnent de 1 à 50. Si la valeur spécifiée par la clé de Registre est supérieure à 50, la valeur maximale est utilisée (50).

