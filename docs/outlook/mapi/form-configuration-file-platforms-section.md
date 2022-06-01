---
title: Section Fichier de configuration de formulaire [Plateformes]
description: Cet article fournit une vue d’ensemble détaillée du fichier de configuration de formulaire [plateformes].
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
ms.openlocfilehash: 22253d6af707bbc8d14936b0f4938e7e4bd5e29d
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817920"
---
# <a name="form-configuration-file-platforms-section"></a>Section Fichier de configuration de formulaire [Plateformes]

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[Plateformes]** répertorie l’ensemble complet de plateformes prises en charge par ce formulaire. Chaque entrée de plateforme se compose de la plateforme de préfixe **.** _chaîne_, où  _string_ est un code de chaîne arbitraire pour la plateforme. Chaque chaîne correspond à l’entrée **du processeur** d’une section **[Plateformes]** individuelle. Chaque entrée d’une section **[Plateformes]** définit une  _chaîne de plateforme_ qui fait référence à une **[plateforme] suivante.** _chaîne de plateforme_ **]** section comme illustré ici. 
  
La section **[Plateformes]** répertorie l’ensemble complet de plateformes prises en charge par ce formulaire. Chaque entrée de plateforme se compose de la plateforme de préfixe **.** _chaîne_, où  _string_ est un code de chaîne arbitraire pour la plateforme. Chaque chaîne correspond à l’entrée **du processeur** d’une section **[Plateformes]** individuelle. Chaque entrée d’une section **[Plateformes]** définit une  _chaîne de plateforme_ qui fait référence à une **[plateforme] suivante.** _chaîne de plateforme_ **]** section comme illustré ici. 
  
**[Plateformes]**
  
**Plateforme**. _String_ =   _chaîne de plateforme_
  
Voici un exemple de section **[Plateformes** ]. 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

Chaque **[plateforme.** _la_ section chaîne de plateforme **]** contient les deux entrées requises, **CPU** et **OSVersion**. L’entrée **du processeur** spécifie le processeur et l’entrée **OSVersion** spécifie le système d’exploitation. Les valeurs **d’UC** valides sont décrites dans le tableau suivant. 
  
|**Entrée du processeur**|**Processeur**|
|:-----|:-----|
|Ix86  <br/> |Processeurs intel 80x86 et Pentium, ainsi que des processeurs équivalents d’AMD, de Cyrix, de NextGen et d’autres fabricants. |
|MIPS  <br/> |Processeurs de la série MIPS R4000. |
|AXP  <br/> |Processeur Alpha AXP de Digital Equipment Corporation. |
|PPC  <br/> |Processeurs de la série Motorola Power PC. |
|M68  <br/> |Processeurs de la série Mororola 68x00. |
   
Les valeurs **OSVersion** valides sont décrites dans le tableau suivant. 
  
|**Entrée OSVersion**|**Système d'exploitation**|
|:-----|:-----|
|Win3.1  <br/> |Windows 3.1 et Windows pour les groupes de travail 3.11. |
|WinNT3.5  <br/> |Windows NT 3.5 ou inférieur. |
|Win95  <br/> |Windows 95. |
|WinNT4.0  <br/> |Windows NT 4.0. |
|Mac7  <br/> |Macintosh System 7. |
   
En outre, [ **Platform.** _la section chaîne de plateforme_ **]** doit contenir une entrée **File** ou **LinkTo** . L’entrée **de** fichier répertorie le fichier exécutable d’application de serveur de formulaires que la bibliothèque de formulaires gère et charge dans un nouveau sous-répertoire du cache de disque au lancement du formulaire. Si une entrée **LinkTo** est utilisée à la place, elle contient le nom d’une autre chaîne de plateforme à partir de laquelle les informations **de fichier** sont extraites. Cela est utile si une version d’un formulaire prend en charge plusieurs plateformes. 
  
L’entrée **de Registre** est utilisée chaque fois que l’entrée **de fichier** est utilisée, elle identifie la clé de Registre pour la bibliothèque de formulaires où le fichier exécutable de l’application de serveur de formulaires est stocké. Les chaînes précédées d’une barre oblique inverse (\ ) sont placées à la racine du registre. Les chaînes non précédées d’une barre oblique inverse sont placées dans la HKEY_CLASSES_ROOT\CLSID\ clé de Registre  _GUID_\, où  _GUID_ est le **GUID** du formulaire. Les caractères « %d » peuvent être utilisés pour indiquer le chemin d’accès du répertoire à partir duquel le fichier de configuration du formulaire a été lu. Cela est utile pour spécifier d’autres fichiers avec des chemins d’accès par rapport au fichier de configuration de formulaire. Plusieurs entrées **de fichier** ou **de Registre** peuvent être spécifiées à l’aide d’un fichier ou d’un Registre comme préfixe suivi de tout autre texte. Format de [ **Platform.** _platform string_ **]** section is: 
  
- **[Plateforme.** _chaîne de plateforme_ **]**
    
- **CPU** =   _String_
    
- **OSVersion** =   _String_
    
- **Fichier** =   _Chemin_
    
- **LinkTo** =   _String_
    
- **Registre** =   _String_
  
Voici deux exemples **[Platform.** _chaîne de plateforme_ **]** sections, l’une utilisant l’entrée **de fichier** et l’autre utilisant l’entrée **LinkTo** . 
  
```cpp
[Platform.NTx86]
CPU = ix86
OSVersion = WinNT3.5
File = \helpdesk.exe
Registry = Local Server = %d\helpdesk.exe
[Platform.Win95]
CPU = ix86
OSVersion = Win95
LinkTo = NTx86

```

**[Plateforme.** _la section chaîne de plateforme_ **]** est ignorée lors de l’ajout d’un formulaire à la bibliothèque de formulaires locale, lorsqu’il est supposé que le programme d’installation a placé les fichiers constituant le gestionnaire de classe de message dans le stockage local disponible, comme indiqué dans la section du gestionnaire dans le registre OLE, et a effectué l’inscription OLE dans le registre du système. 
  

