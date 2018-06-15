---
title: Choisissez une version spécifique de MAPI à charger
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d0bce7b3a12f259b7ac5f28219c8a92dd2200f07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19783459"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a>Choisissez une version spécifique de MAPI à charger

**S’applique à**: Outlook 
  
Lors de la liaison explicite à une implémentation de MAPI, vous devez sélectionner avec soin l’implémentation à charger. 
  
Il existe deux méthodes pour lier explicitement à une implémentation de MAPI. 
  
1. Vous pouvez charger la bibliothèque stub MAPI et spécifier dans le Registre des appels vers une DLL personnalisée pour charger et distribuer MAPI.
    
2. Vous pouvez implémenter l’algorithme de recherche MAPI client pour rechercher la version de MAPI utilisé par le client de messagerie par défaut et le charger.
    
Étant donné que vous pouvez modifier les [Paramètres de Registre Stub Mapi32.dll](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx) pour diriger votre application pour utiliser une implémentation de MAPI, nous vous recommandons de rediriger votre application pour utiliser une implémentation de MAPI que vous avez testé avec. La liste suivante décrit les deux méthodes de liaison explicite. 
  
## <a name="reading-from-the-registry"></a>Lecture à partir du Registre

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>Pour lire les informations de mise en œuvre de MAPI à partir du Registre

1. Les clés de Registre qui indiquent une DLL personnalisée pour un client de messagerie sont situés sous le `HKLM\Software\Clients\Mail` clés du client de messagerie. 
    
   Le tableau suivant décrit ces clés :
    
   |**Clé**|**Description**|
   |:-----|:-----|
   |MSIComponentID  <br/> |Une catégorie de Windows Installer PublishComponent ID (GUID) qui identifie la DLL qui exporte simple MAPI ou MAPI appelle. Si définie, cette clé est prioritaire sur la touche **DLLPath** ou **DLLPathEx** .  <br/> |
   |MSIApplicationLCID  <br/> |Identificateur de paramètres régionaux (LCID) pour votre application. La première chaîne de valeur identifie une sous-clé à partir de `HKLM\Software` et valeurs de chaîne suivantes identifient les valeurs de Registre qui contiennent des informations de paramètres régionaux sous cette clé.  <br/> |
   |MSIOfficeLCID  <br/> |LCID pour Microsoft Office. La première chaîne de valeur identifie une sous-clé à partir de `HKLM\Software` et valeurs de chaîne suivantes identifient les valeurs sous cette clé de Registre.  <br/> |
   
   Obtenir les informations à partir de ces clés.
    
2. Transmettre les valeurs que vous avez obtenu à partir de l’étape précédente à la fonction [FGetComponentPath](fgetcomponentpath.md) . **FGetComponentPath** est une fonction qui est exportée par la bibliothèque de stub MAPI Mapistub.dll. Elle renvoie le chemin d’accès de la version personnalisée de MAPI. 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>Pour charger l’implémentation de MAPI marqué comme valeur par défaut

1. Lire la `HKLM\Software\Clients\Mail::(default)` valeur de Registre. 
    
2. Rechercher des informations pour le client indiqué comme décrit précédemment.
    
> [!NOTE]
> Notez que le client de messagerie par défaut ne peut pas implémenter interface MAPI étendue. 
  
#### <a name="example"></a>Exemple

Pour charger MAPI telle qu’implémentée par Outlook, rechercher les clés de Registre sous `HKLM\Software\Clients\Mail\Microsoft Outlook` et transmettez-les à **FGetComponentPath**. **FGetComponentPath** renvoie le chemin d’accès pour l’implémentation d’Outlook de MAPI. 
  
Si les clés de **MSIComponentID**, **MSIApplicationLCID**et **MSIOfficeLCID** ne sont pas définies, vérifiez la valeur de Registre **DLLPathEx** . Si les clés sont définies, **FGetComponentPath** donne le chemin d’accès de l’implémentation du client de MAPI. 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>L’implémentation de l’algorithme de recherche de clients MAPI

Le tableau suivant répertorie les quatre fonctions de MFCMAPI qui sont utilisées pour rechercher le chemin d’accès d’une implémentation personnalisée de MAPI :
  
|**Fonction**|**Description**|
|:-----|:-----|
| `GetMAPIPath` <br/> |Obtient le chemin d’accès de la bibliothèque MAPI.  <br/> |
| `GetMailKey` <br/> |Obtient la clé de Registre de messagerie MAPI.  <br/> |
| `GetMapiMsiIds` <br/> |Obtient l’identificateur de Windows Installer.  <br/> |
| `GetComponentPath` <br/> |Obtient le chemin d’accès du composant à l’aide de [FGetComponentPath](fgetcomponentpath.md).  <br/> |
   
Car MFCMAPI charge l’implémentation par défaut de MAPI par défaut, si vous souhaitez utiliser une autre implémentation de MAPI, vous devez explicitement lui à le faire. Cette opération est effectuée à l’aide de la routine **Session\Load MAPI** . 
  
### <a name="how-these-functions-work"></a>Fonctionnement de ces fonctions.

1. Appels MFCMAPI `GetMAPIPath`, passant NULL pour le paramètre client, pour charger l’implémentation de MAPI par défaut.
    
2.  `GetMAPIPath`appels `GetMapiMsiIds` pour lire les valeurs pour **MSIComponentID**, **MSIApplicationLCID**et **MSIOfficeLCID**.
    
3.  `GetMapiMsiIds`appels `GetMailKey` pour ouvrir la clé de Registre pour le client de messagerie par défaut. 
    
4.  `GetMapiMsiIds`utilise le handle de Registre retourné par `GetMailKey` pour rechercher des valeurs pour **MSIComponentID**, **MSIApplicationLCID**et **MSIOfficeLCID**.
    
5. Les valeurs de **MSIComponentID**, **MSIApplicationLCID**et **MSIOfficeLCID**, sont renvoyés à `GetMAPIPath`.  `GetMAPIPath`transmet à `GetComponentPath`.
    
6.  `GetComponentPath`charge la bibliothèque stub MAPI, Mapi32.dll, à partir du répertoire du système. 
    
7.  `GetComponentPath`puis extrait l’adresse de la fonction **FGetComponentPath** Mapi32.dll, en supposant que Mapi32.dll exporte **FGetComponentPath**.
    
8. Si l’obtention de l’adresse de **FGetComponentPath** à partir de Mapi32.dll échoue, `GetComponentPath` récupère l’adresse Mapistub.dll. 
    
9.  `GetComponentPath`appelle ensuite **FGetComponentPath**, obtenir le chemin d’accès de la version par défaut de MAPI.
    
10.  `GetMAPIPath`renvoie ensuite ce chemin d’accès à l’appelant, puis charge MAPI et lie explicitement lui comme décrit dans [le lien fonctions MAPI](how-to-link-to-mapi-functions.md).
    
> [!NOTE] 
> - Pour prendre en charge les copies localisées de MAPI pour l’anglais et les paramètres régionaux non anglais, `GetMAPIPath` lit les valeurs pour les sous-clés **MSIApplicationLCID** et **MSIOfficeLCID** .  `GetMAPIPath`appelle ensuite **FGetComponentPath**, tout d’abord spécifiant **MSIApplicationLCID** sous **szQualifier**, puis à nouveau spécifiant **MSIOfficeLCID** comme **szQualifier**. Pour plus d’informations sur les clés de Registre pour les clients de messagerie qui prennent en charge des langues, voir [Paramètre Up the MSI clés pour votre DLL MAPI](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx).   
> - Si MFCMAPI ne reçoit pas d’un chemin d’accès pour l’utilisation de MAPI `GetMAPIPath`, il charge la bibliothèque de stub MAPI à partir du répertoire du système.
> - La valeur de Registre **MSMapiApps** présentée dans le [Mappage explicitement des appels MAPI aux DLL MAPI](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx) s’applique uniquement lorsque la bibliothèque Stub MAPI est utilisée. Applications qui chargement une implémentation de MAPI ou chargement l’implémentation par défaut n’ont pas définir la clé de Registre **MSMapiApps** . 
    
## <a name="see-also"></a>Voir aussi

- [FGetComponentPath](fgetcomponentpath.md)
- [Vue d'ensemble de la programmation MAPI](mapi-programming-overview.md)
- [Lien vers des fonctions MAPI](how-to-link-to-mapi-functions.md)
- [Paramètres de Registre Stub Mapi32.dll](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx)
- [Configuration des clés MSI pour votre DLL MAPI](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx)
- [Mappage explicitement des appels MAPI aux DLL MAPI](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx)

