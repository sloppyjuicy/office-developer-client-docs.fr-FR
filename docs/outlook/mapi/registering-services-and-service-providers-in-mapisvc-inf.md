---
title: Inscription des services et des fournisseurs de services dans MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Dernière modification: 18 juillet 2013'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328370"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>Inscription des services et des fournisseurs de services dans MapiSvc. inf

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'installation d'un nouveau fournisseur sur un système nécessite de mettre à jour le fichier MapiSvc. inf afin de pointer vers le nouveau fournisseur. Les propriétés standard définies lors de la configuration, notamment les suivantes, informent MAPI où trouver la bibliothèque de liens dynamiques (. dll) du fournisseur:
  
- Le **PR_SERVICE_DLL_NAME** est spécifié dans la section **[message service]** . 
    
- Le **PR_PROVIDER_DLL_NAME** est spécifié dans la section **[Service Provider]** . 
    
> [!NOTE]
> L'attente est que vous définissez le nom du fichier. dll de votre fournisseur (sans le suffixe «32»). MAPI charge ensuite votre fournisseur en le recherchant sur le chemin d'accès. 
  
## <a name="putting-a-path-in-mapisvcinf"></a>Placement d'un chemin d'accès dans MapiSvc. inf

La plupart des applications sont installées sous Program Files, ce qui nécessite une mise à jour de la variable PATH pour permettre aux fournisseurs MAPI de fonctionner. Avec quelques restrictions, Microsoft Outlook 2010 et Outlook 2013 peuvent prendre en charge les chemins d'accès complets aux fournisseurs MAPI.
  
Lors de l'inscription de votre fournisseur dans MapiSvc. inf, vous pouvez placer le chemin d'accès complet au fournisseur dans les propriétés MAPI **PR_SERVICE_DLL_NAME** et **PR_PROVIDER_DLL_NAME**.
  
Dans l'une ou l'autre de ces propriétés, le chemin d'accès complet doit être sans le suffixe «32», car MAPI continue à l'ajouter au nom de fichier avant de consulter votre fichier. Cela signifie que si vous enregistrez le chemin d'accès «c:\mypath\myprovider.dll», MAPI tentera de charger «c:\mypath\myprovider32.dll».
  
Étant donné que l'interface MAPI d'Outlook n'a pas été conçue à l'origine pour prendre en charge les chemins d'accès complets, elle permet d'insérer le suffixe «32» en recherchant la première période dans la chaîne, ce qui signifie que les chemins d'accès qui contiennent d'autres périodes ne fonctionnent pas, de sorte que vous ne pouvez pas utiliser des chemins d'accès tels que «c:\My.path\myprovider.dll» ou «c:\mypath\my.Provider.dll».
  
Parfois, dans un fournisseur de banque, vous allez générer des identificateurs d'entrée à l'aide de la fonction **WrapStoreEntryID** , qui prend comme paramètre le nom de votre fournisseur. 
  
> [!IMPORTANT]
> Si vous utilisez des chemins d'accès complets dans MapiSvc. inf, vous devez utiliser le même chemin d'accès dans les appels à **WrapStoreEntryID**. 
  
De plus, le chemin d'accès que vous utilisez peut être converti vers et à partir d'Unicode à l'aide de la page de code fournie par la fonction [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) . 
  
> [!CAUTION]
> Une erreur se produit si vous choisissez un chemin d'accès contenant des caractères qui ne peuvent pas survivre à une telle boucle via les fonctions [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) et [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) . 
  
Pour une démonstration de cette fonctionnalité, l' [exemple de fichier PST encapsulé](https://github.com/stephenegriffin/Outlook2010CodeSamples) sur GitHub a été modifié: les fonctionnalités pertinentes se trouvent dans **MergeWithMapiSvc** et **GenerateProviderPath**.
  

