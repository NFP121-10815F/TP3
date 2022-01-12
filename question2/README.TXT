public boolean equals(Object o) {
    if (o instanceof PileI) {
      PileI p = (PileI) o;
      return this.capacite() == p.capacite()
          && this.hashCode() == p.hashCode();
    } else
      return false;
    }
    Cette réponse est correcte si l'on ne veut pas tester le type de l'objet 
    Or 1 != "1"
 
    La règle à retenir est : 
	Deux piles sont égales si elles ont la même taille, 
	même capacité, et les éléments contenus identiques.
 
    Cette autre réponse n'est pas correcte

    public boolean equals(Object o) {
        return this.toString().equals(o.toString());
    }

     On teste l'égalité que sur la façon dont elle est écrite à l'écran.
     On ne teste pas la taille ni la capacité ni le type de l'objet.