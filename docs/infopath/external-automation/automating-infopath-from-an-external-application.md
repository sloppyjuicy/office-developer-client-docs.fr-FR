---
title: Automatisation d’InfoPath à partir d’une application externe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath fournit l’automatisation de l’application à partir du code écrit à l’aide de COM et d’un script à l’aide des méthodes de l’objet Application et de la collection XDocuments.
ms.openlocfilehash: bc69fedbdede83b85a1b9e63a522dc5a60fe9cc7
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772316"
---
# <a name="automating-infopath-from-an-external-application"></a>Automatisation d’InfoPath à partir d’une application externe

Microsoft InfoPath fournit l’automatisation de l’application à partir du code écrit à l’aide de COM et d’un script à l’aide des méthodes de l’objet **Application** et de la collection **XDocuments** . 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>Vue d’ensemble des objets Application et XDocument

**L’objet Application** contient les méthodes suivantes utilisées pour l’automatisation : 
  
|**Méthode**|**Description**|
|:-----|:-----|
|**CacheSolution** <br/> |Examine le contenu du cache et, si nécessaire, le met à jour à partir de l’emplacement publié du modèle de formulaire. |
|**Quit** <br/> |Quitte l’Microsoft Office’application InfoPath. |
|**RegisterSolution** <br/> |Installe le modèle de formulaire InfoPath Microsoft Office spécifié. |
|**UnregisterSolution** <br/> |Désinstalle le modèle de formulaire InfoPath Microsoft Office spécifié. |
   
La collection **XDocuments** contient les méthodes suivantes qui peuvent être utilisées pour l’automatisation externe : 
  
|**Méthode**|**Description**|
|:-----|:-----|
|Méthode **Close**  <br/> |Ferme le formulaire InfoPath Microsoft Office spécifié. |
|**Nouvelle** méthode  <br/> |Crée une nouvelle Microsoft Office formulaire InfoPath. |
|**Méthode NewFromSolution**  <br/> |Crée un nouveau Microsoft Office Formulaire InfoPath basé sur le modèle de formulaire spécifié. |
|**Méthode NewFromSolutionWithData**  <br/> |Crée une nouvelle Microsoft Office formulaire InfoPath à l’aide des données XML et du modèle de formulaire spécifiés. |
|**Open,** méthode  <br/> |Ouvre le formulaire InfoPath Microsoft Office spécifié. |
   
Pour utiliser l’objet **Application** d’une application externe, utilisez la fonction **CreateObject** avec le ProgID de l’application InfoPath (« InfoPath.Application ») pour créer une variable objet qui représente l’application InfoPath. Vous pouvez ensuite utiliser la **propriété XDocuments** pour accéder à la collection **XDocuments** et utiliser ses méthodes pour ouvrir ou créer un formulaire InfoPath. L’exemple suivant illustre la création d’une référence à l’objet **Application** à l’aide du langage de programmation Microsoft Visual Basic 6.0 ou Visual Basic pour Applications (VBA) : 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> Étant donné que **la fonction CreateObject** crée une variable objet à l’aide de la liaison tardive, l’achèvement automatique de l’instruction ne sera pas disponible dans l’éditeur Visual Basic. Reportez-vous aux liens des tableaux précédents pour plus d’informations sur la syntaxe d’appel correcte. 
  

